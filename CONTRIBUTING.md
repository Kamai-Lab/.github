# Cómo se trabaja en Kamai-Lab

## Nomenclatura de repos
`cliente-proyecto` — en minúsculas, sin espacios. Ejemplo: `laofrenda-conciliacion`.

## Al crear un repo nuevo
GitHub no conecta un repo nuevo a ningún team automáticamente. Paso manual obligatorio:

1. Settings del repo → **Collaborators and teams**
2. **Add teams** → elegí el team correspondiente (`implementin-devs`, `implementex-devs`, `vibecodianos-devs`)
3. Asigná permiso **Write**

## CODEOWNERS
Todo repo con trabajo real necesita su propio `.github/CODEOWNERS` (no se hereda desde este repo). Antes de nombrar a alguien ahí, confirmá que tiene Write explícito en ese repo puntual — sin eso, GitHub no lo pide como reviewer.

## Formato de commits
Conventional commits: `tipo(alcance): descripción`. Tipos válidos: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`.

## Flujo de labels en un issue
`status:needs-review` (recién creado) → `status:assigned` (tiene owner y arrancó) → `status:approved` (listo para PR).

## Templates
No se abren issues en blanco salvo que seas maintainer. Usá el template que corresponda: bug, feature, o tarea asignada.
