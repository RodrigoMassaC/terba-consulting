# GitHub Setup Instructions

El repositorio Git local ha sido inicializado. Para crear el repositorio en GitHub, sigue estos pasos:

## Opción 1: Usando GitHub Web Interface

1. Ve a https://github.com/new
2. Crea un nuevo repositorio con estos valores:
   - **Repository name**: `terba-consulting`
   - **Description**: "Professional consulting firm website - Terba Consulting"
   - **Visibility**: Public
   - **DO NOT** inicializar con README, .gitignore, o licencia (ya los tenemos localmente)

3. Después de crear el repositorio, ejecuta estos comandos en tu terminal:

```bash
cd ~/Desktop/terba-consulting
git remote add origin https://github.com/[TU_USUARIO]/terba-consulting.git
git branch -M main
git push -u origin main
```

Reemplaza `[TU_USUARIO]` con tu username de GitHub.

## Opción 2: Usando GitHub CLI (gh)

Si tienes GitHub CLI instalado:

```bash
cd ~/Desktop/terba-consulting
gh repo create terba-consulting --source=. --remote=origin --push --public --description "Professional consulting firm website - Terba Consulting"
```

## Opción 3: Usando SSH

Si prefieres usar SSH en lugar de HTTPS:

```bash
cd ~/Desktop/terba-consulting
git remote add origin git@github.com:[TU_USUARIO]/terba-consulting.git
git branch -M main
git push -u origin main
```

## Después de crear el repositorio

### Habilitar GitHub Pages (opcional pero recomendado)

1. Ve a Settings → Pages
2. Selecciona "Deploy from a branch"
3. Selecciona `main` como rama
4. Tu sitio estará disponible en: `https://[tu_usuario].github.io/terba-consulting`

### Configuración recomendada

En Settings:
- ✅ Discussions (para feedback de clientes)
- ✅ Wiki (para documentación interna)
- ✅ Require a pull request review before merging
- ✅ Require branches to be up to date before merging

## Verificar que funcionó

```bash
cd ~/Desktop/terba-consulting
git remote -v  # Debería mostrar origin con tu URL
git log        # Debería mostrar el commit inicial
```

---

Una vez creado el repositorio, puedes hacer push de cambios futuros con:
```bash
git add .
git commit -m "tu mensaje"
git push
```
