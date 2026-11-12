# EXODU'S Gestão 3D — Next.js

## Executar localmente

1. Instale Node.js (versão 20 ou superior).
2. Copie `.env.example` para `.env.local`.
3. Preencha as variáveis com as credenciais do seu app Firebase.
4. No terminal, dentro desta pasta, execute:

```bash
npm install
npm run dev
```

5. Abra http://localhost:3000.

## Firebase obrigatório

No Firebase Console:
- Crie ou selecione um projeto e registre um aplicativo Web.
- Copie as credenciais do SDK para `.env.local`.
- Em Authentication > Sign-in method, habilite **Anonymous**.
- Crie o Firestore Database.
- Configure as regras do Firestore para permitir acesso somente aos dados autenticados e valide-as antes de produção.

## Publicar no Vercel

Envie esta pasta para um repositório GitHub e importe o repositório no Vercel.
No Vercel, em Settings > Environment Variables, cadastre as mesmas variáveis `NEXT_PUBLIC_FIREBASE_*` do `.env.local`.
Depois faça um novo Deploy.

O app usa o caminho `artifacts/{namespace}/users/{uid}/...` no Firestore.
