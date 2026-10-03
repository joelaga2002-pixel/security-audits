# 🤝 Guía de Contribución

Gracias por considerar contribuir a **Security Audits**. Este documento proporciona pautas y instrucciones para colaborar efectivamente.

## 📋 Tabla de Contenidos

1. [Código de Conducta](#código-de-conducta)
2. [Cómo Contribuir](#cómo-contribuir)
3. [Proceso de Pull Request](#proceso-de-pull-request)
4. [Estándares de Calidad](#estándares-de-calidad)
5. [Reportar Bugs](#reportar-bugs)
6. [Sugerir Mejoras](#sugerir-mejoras)

---

## 🎯 Código de Conducta

### Nuestro Compromiso

Nos comprometemos a proporcionar un ambiente acogedor y libre de discriminación para todos los participantes.

### Comportamiento Esperado

- Sé respetuoso y considerado
- Acepta críticas constructivas
- Enfócate en lo mejor para la comunidad
- Muestra empatía hacia otros miembros

### Comportamiento Inaceptable

- Lenguaje o imágenes ofensivas
- Ataques personales o insultos
- Acoso público o privado
- Publicación de información privada sin consentimiento

---

## 🚀 Cómo Contribuir

### 1. Fork el Repositorio

```bash
# En GitHub, haz clic en "Fork" en la esquina superior derecha
# O usa GitHub CLI:
gh repo fork joelaga2002-pixel/security-audits --clone
```

### 2. Crea una Rama de Feature

```bash
git checkout -b feature/tu-feature-descriptiva
```

Nombres de rama recomendados:
- `feature/nueva-funcionalidad`
- `fix/correccion-bug`
- `docs/mejora-documentacion`
- `perf/optimizacion-performance`

### 3. Realiza tus Cambios

```bash
# Edita archivos
git add .
git commit -m "feat: Descripción clara del cambio"
```

### 4. Sincroniza con Upstream

```bash
git fetch upstream
git rebase upstream/master
```

### 5. Push a tu Fork

```bash
git push origin feature/tu-feature-descriptiva
```

### 6. Abre un Pull Request

En GitHub:
- Título claro y descriptivo
- Descripción detallada de cambios
- Referencia a issues relacionados
- Screenshots (si aplica)

---

## 📋 Proceso de Pull Request

### Checklist Previo

Antes de abrir un PR, verifica:

- [ ] Mi código sigue los estándares del proyecto
- [ ] He ejecutado pruebas locales (si aplica)
- [ ] He actualizado la documentación
- [ ] Mis commits tienen mensajes claros
- [ ] No he introducido cambios no relacionados
- [ ] El código está libre de credenciales/secrets

### Formato de Commit

```
<tipo>(<scope>): <descripción>

<cuerpo opcional>

<footer opcional>

Tipos permitidos:
- feat: Nueva característica
- fix: Corrección de bug
- docs: Cambios en documentación
- style: Formato, espacios en blanco
- refactor: Refactorización sin cambio funcional
- perf: Mejora de performance
- test: Adición de tests
- ci: Cambios en CI/CD
- chore: Cambios en dependencias, build, etc.
```

### Ejemplo

```
feat(audits): Add automated vulnerability scanning

Implement automated SAST scanning for pull requests using
industry-standard tools. This enables early detection of
security issues in the audit workflow.

Closes #123
Relates to #456
```

---

## ✅ Estándares de Calidad

### Documentación

- [ ] README.md actualizado
- [ ] Cambios en APIs documentados
- [ ] Ejemplos de uso proporcionados
- [ ] Comentarios en código complejo

### Código

- [ ] Código limpio y legible
- [ ] Sin warnings o errores
- [ ] Funciones pequeñas y enfocadas
- [ ] Sin código muerto

### Seguridad

- [ ] No incluye credenciales hardcodeadas
- [ ] No expone información sensible
- [ ] Sigue OWASP guidelines
- [ ] Validación de entrada apropiada

---

## 🐛 Reportar Bugs

### Antes de Reportar

1. Revisa issues existentes (abiertos y cerrados)
2. Actualiza a la última versión
3. Verifica si es un problema de configuración local

### Creando un Reporte de Bug

**Usa este template:**

```markdown
### Descripción
Breve descripción de lo que pasó

### Pasos para Reproducir
1. Paso 1
2. Paso 2
3. ...

### Comportamiento Esperado
Qué debería haber pasado

### Comportamiento Actual
Qué pasó en realidad

### Entorno
- OS: [Windows/macOS/Linux]
- Navegador: [Chrome/Firefox/Safari]
- Rama: [master/develop/etc]

### Logs o Screenshots
Adjunta logs relevantes o screenshots

### Información Adicional
Cualquier otro contexto
```

---

## 💡 Sugerir Mejoras

### Template para Feature Requests

```markdown
### Descripción de la Mejora
Descripción clara de lo que quieres que se implemente

### Contexto
Por qué crees que esta mejora es importante

### Solución Propuesta
Cómo imaginas que funcionaría

### Alternativas Consideradas
Otras formas en que se podría resolver esto

### Contexto Adicional
Ejemplos, links, etc.
```

---

## 📚 Estructura de Proyecto

```
security-audits/
├── .github/
│   └── workflows/           # CI/CD workflows
├── reports/                 # Reportes de auditoría
├── vulnerabilities/         # Base de conocimiento
├── best-practices/          # Guías y documentación
└── tools/                   # Scripts y utilidades
```

---

## 🔍 Review Process

### Lo que Esperamos

1. **Revisión Automática**
   - Workflows de CI/CD pasan
   - Validación forense exitosa
   - Auditoría de seguridad OK

2. **Revisión Manual**
   - Mínimo 1 maintainer aprueba
   - Comentarios resueltos
   - Tests pasan

3. **Merge**
   - Squash commit (por defecto)
   - Rama se elimina
   - Issue se cierra automáticamente

---

## 🎓 Desarrollo Local

### Requisitos

- Git
- GitHub CLI (opcional pero recomendado)
- Editor de texto/IDE

### Setup Inicial

```bash
# Clonar
git clone https://github.com/joelaga2002-pixel/security-audits.git
cd security-audits

# Configurar upstream
git remote add upstream https://github.com/anza-xyz/security-audits.git
git fetch upstream

# Verificar
git remote -v
```

### Ejecutar Validaciones Locales

```bash
# Verificar estructura
[ -f "README.md" ] && echo "✅ README OK"
[ -f "LICENSE" ] && echo "✅ LICENSE OK"

# Validar YAML
yamllint .github/workflows/

# Ver cambios
git diff
git status
```

---

## 🚫 Lo Que NO Hacer

❌ No commits directos a `master`  
❌ No force push a ramas compartidas  
❌ No archivos generados automáticamente  
❌ No cambios de versión sin coordinación  
❌ No código sin documentar  
❌ No PRs enormes (máx 400 líneas)  

---

## 📞 Preguntas o Necesitas Ayuda?

- **Abre una Discussion**: Para preguntas generales
- **Crea un Issue**: Para bugs o mejoras
- **Revisa el Wiki**: Para documentación completa
- **Contacta al Maintainer**: @joelaga2002-pixel

---

## ✨ Agradecimientos

Tu contribución es invaluable. Apreciamos tu tiempo y esfuerzo en mejorar este proyecto.

---

**Última actualización**: Octubre 3, 2026  
**Versión**: 1.0
