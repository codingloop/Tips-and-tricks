### Debug RLS in supabase
```
set local role authenticated;

-- inject fake JWT claims - for sub, add actual uuid
set local "request.jwt.claims" = '{"role": "authenticated", "sub": "3333-2222-2222-2222-222222222"}';

select auth.uid();
```
