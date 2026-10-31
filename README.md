# MovieSeriesManagement · Sistema de gestión de películas y series

Proyecto de aplicación web realizado con **C#, ASP.NET Core MVC (.NET 8), ASP.NET Core Identity, Entity Framework Core y SQL Server**.

## Funciones presentes en el código
- Gestión de películas y series, con búsquedas y filtros
- Administración de contenido mediante roles
- Registro del historial de visualización
- Lógica de recomendaciones basada en preferencias de género y popularidad
- Servicios y repositorios para separar lógica de negocio y persistencia

El sistema de recomendaciones aplica reglas explícitas, no aprendizaje automático.

## Seguridad y estado de revisión
Esta rama elimina una contraseña fija de administrador. La creación de una cuenta administrativa de prueba está deshabilitada de forma predeterminada y solo se habilita expresamente en **Development**, utilizando configuración externa (`SeedAdmin__Enabled`, `SeedAdmin__Email`, `SeedAdmin__Password`). No se debe usar en producción.

Todavía se necesita ejecutar compilación, pruebas funcionales, revisar archivos subidos por usuarios, dependencias y configuración antes de desplegar. No se afirma que sea un producto listo para producción.

## Para ejecutar localmente
1. Instalar .NET SDK 8 y SQL Server.
2. Configurar `ConnectionStrings:DefaultConnection` mediante secretos de desarrollo o variables de entorno.
3. Aplicar las migraciones Entity Framework existentes y comprobar que la base de datos corresponda al modelo.
4. Ejecutar:
```bash
dotnet restore MovieSeriesManagement/MovieSeriesManagement.csproj
dotnet run --project MovieSeriesManagement
```

**Autor:** Andrés Araya · [GitHub](https://github.com/andresarzz)
