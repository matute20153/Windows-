# Instalación de Windows 11 en equipos no compatibles (Bypass TPM y Secure Boot)

## 📌 Descripción
En esta documentación detallo el procedimiento utilizado para instalar **Windows 11** en equipos que no cumplen con los requisitos oficiales de **TPM 2.0** y **Secure Boot**, utilizando métodos de bypass durante la instalación.

Este procedimiento fue realizado con fines **laborales**, en equipos propios o con autorización del cliente / usuario.

---

## ⚙️ Escenario
Durante la instalación de Windows 11, el sistema muestra el mensaje de incompatibilidad debido a:
- Ausencia de TPM 2.0
- Secure Boot deshabilitado o no soportado
- Hardware antiguo pero funcional

---

## 🛠️ Herramientas utilizadas
- Imagen ISO oficial de Windows 11
- Medio de instalación USB
- Editor de registro (regedit)
- Entorno de instalación de Windows (WinPE)

---

## 🔧 Procedimiento (resumen técnico)

1. Iniciar el equipo desde el medio de instalación de Windows 11.
2. Al aparecer el mensaje de incompatibilidad, presionar:
s- SHIFT + F10 para abrir la consola
Ejecutar: REGEDIT
4. Navegar a la clave:
HKEY_LOCAL_MACHINE\SYSTEM\Setup

5. Crear una nueva clave llamada:
LabConfig

6. Dentro de `LabConfig`, crear los siguientes valores DWORD (32 bits):
- `BypassTPMCheck` = 1
- `BypassSecureBootCheck` = 1

7. Cerrar el editor de registro y continuar con la instalación normalmente.

---

## ✅ Resultado
La instalación de Windows 11 se completa correctamente en hardware no compatible, manteniendo estabilidad y funcionamiento normal del sistema operativo.

---

## ⚠️ Consideraciones
- Microsoft no garantiza actualizaciones en equipos no compatibles.
- El procedimiento debe utilizarse únicamente en entornos controlados.
- No se recomienda para equipos de producción sin evaluación previa.

---

## 🧠 Conclusión
Este procedimiento permite extender la vida útil de hardware funcional, aplicando conocimientos técnicos de sistemas operativos, diagnóstico de compatibilidad y resolución de problemas durante instalaciones.


