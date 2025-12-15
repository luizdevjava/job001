# Acompanhantes VIP

Site moderno e intuitivo de anúncios de acompanhantes, desenvolvido com Next.js 15, TypeScript, Tailwind CSS e Prisma.

## 🚀 Funcionalidades

### Página Principal
- **Slider de Destaques**: Exibe até 3 anúncios em destaque com navegação automática
- **Galeria de Anúncios**: Grid responsivo com todos os anúncios ativos
- **Sistema de Filtros**: Filtre por tags e bairro
- **Design Responsivo**: Mobile-first com layout adaptativo

### Página do Anúncio
- **Galeria de Imagens**: Até 5 fotos com navegação por thumbnails
- **Vídeo Embed**: Suporte para 1 vídeo via URL
- **Informações Completas**: Nome, descrição, tags, bairro
- **Anúncios Relacionados**: Slider lateral e seção final com outros destaques

### Painel Administrativo
- **Login Seguro**: Autenticação via JWT
- **CRUD Completo**: Criar, editar, ativar/desativar, excluir anúncios
- **Gestão de Destaques**: Marcar/desmarcar anúncios como destaque
- **Interface Intuitiva**: Dashboard com estatísticas e gerenciamento visual

## 🛠️ Tecnologias

- **Frontend**: Next.js 15, TypeScript, Tailwind CSS, shadcn/ui
- **Backend**: Next.js API Routes, Prisma ORM
- **Banco de Dados**: SQLite (desenvolvimento) / PostgreSQL (produção)
- **Autenticação**: JWT com bcryptjs
- **Imagens**: URLs externas (sem upload)
- **Deploy**: Vercel compatível

## 📋 Instalação e Configuração

### 1. Clonar o projeto
```bash
git clone <repositório>
cd acompanhantes-vip
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente
Criar arquivo `.env`:
```env
DATABASE_URL="file:./dev.db"
JWT_SECRET="seu-secret-key-aqui"
NEXT_PUBLIC_SITE_URL="https://seu-dominio.com"
```

### 4. Configurar banco de dados
```bash
npm run db:generate
npm run db:push
npm run db:seed
```

### 5. Executar o projeto
```bash
npm run dev
```

## 🔐 Credenciais de Acesso

### Admin
- **Email**: admin@acompanhantes.com
- **Senha**: admin123

> ⚠️ **Importante**: Altere as credenciais em produção usando o painel admin ou diretamente no banco.

## 📁 Estrutura do Projeto

```
src/
├── app/                    # Páginas Next.js
│   ├── api/               # APIs REST
│   │   ├── anuncios/      # CRUD de anúncios
│   │   └── auth/          # Autenticação
│   ├── admin/             # Painel administrativo
│   ├── anuncio/[id]/      # Página individual
│   └── page.tsx           # Página principal
├── components/            # Componentes React
│   ├── ui/               # shadcn/ui components
│   ├── AnuncioCard.tsx   # Card de anúncio
│   ├── Filters.tsx        # Sistema de filtros
│   └── Slider.tsx         # Slider de destaques
├── hooks/                # Hooks personalizados
│   └── useAnuncios.ts     # Hook para buscar anúncios
└── lib/                  # Utilitários
    └── db.ts             # Cliente Prisma
```

## 🎨 Personalização

### Cores
O tema usa roxo como cor principal. Para alterar:
- Procure por `purple-600` nos arquivos CSS/TSX
- Altere para a cor desejada (ex: `pink-600`, `blue-600`)

### Tags e Bairros
Edite o componente `Filters.tsx` para personalizar:
- Tags disponíveis
- Lista de bairros
- Categorias de filtros

## 📱 Deploy

### Vercel (Recomendado)
1. Conecte o repositório ao Vercel
2. Configure as variáveis de ambiente
3. Deploy automático

### Outras plataformas
1. Build do projeto: `npm run build`
2. Configure o banco de dados PostgreSQL
3. Ajuste a variável `DATABASE_URL`
4. Inicie com: `npm start`

## 🔧 Manutenção

### Backup do Banco
```bash
# Para SQLite
cp db/dev.db backup/dev-$(date +%Y%m%d).db

# Para PostgreSQL
pg_dump nome_do_banco > backup.sql
```

### Atualizar Dados
```bash
# Resetar e popular novamente
npm run db:reset
npm run db:seed
```

## 📝 Features Futuras

- [ ] Sistema de favoritos
- [ ] Avaliações e comentários
- [ ] Busca avançada
- [ ] Sistema de denúncias
- [ ] Notificações push
- [ ] App mobile PWA

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch: `git checkout -b feature/nova-feature`
3. Commit suas mudanças: `git commit -m 'Add nova feature'`
4. Push: `git push origin feature/nova-feature`
5. Abra um Pull Request

## 📄 Licença

Este projeto é privado e proprietário. Todos os direitos reservados.

## ⚠️ Aviso Legal

Este site é uma plataforma de anúncios e não se responsabiliza pelo conteúdo publicado. 
Todos os anúncios são de responsabilidade exclusiva dos anunciantes.
É proibido o acesso por menores de 18 anos.

---

**Desenvolvido com ❤️ usando Next.js 15**