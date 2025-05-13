<center><h1><span style="color:green">Code Spaces</span></h1></center>
GitHub Codespaces es un entorno de desarrollo en la nube totalmente integrado con GitHub, que te permite comenzar a programar de inmediato, sin necesidad de instalar herramientas o dependencias en tu equipo local. Cada codespace es una instancia de entorno de desarrollo basada en contenedores Docker que se ejecuta en una máquina virtual en la infraestructura de GitHub.  
Cada espacio de código que crees se aloja en GitHub en un contenedor Docker, ejecutándose en una máquina virtual. Puedes elegir entre varios tipos de máquinas virtuales, desde 2 núcleos, 8 GB de RAM y 32 GB de almacenamiento, hasta 32 núcleos, 64 GB de RAM y 128 GB de almacenamiento.

# Uso de GitHub Codespaces  
GitHub Codespaces te permite crear un espacio de código (codespace) a partir de una plantilla  o de cualquier rama o commit de un repositorio existente. Esto te da flexibilidad para empezar desde cero o trabajar con una versión específica del código.  
1. Crear un codespace desde un repositorio:  
- Ve al repositorio en GitHub.  
- Haz clic en el botón verde "Code" y luego en "Codespaces".  
- Selecciona "New codespace" y elige la rama desde la cual quieres iniciar.  
- GitHub creará el entorno de desarrollo automáticamente.  
2. Crear un codespace desde una plantilla:  
- Ve a github.com/codespaces y elige una plantilla prediseñada o en blanco.  
- Ideal para crear proyectos nuevos con una base preconfigurada.  
3. Reabrir un codespace existente:  
- Desde GitHub, visita la pestaña "Codespaces" de tu perfil o del repositorio.  
- Allí verás todos tus codespaces disponibles y podrás reabrir cualquiera.  

# Personalización de GitHub Codespaces
GitHub Codespaces permite crear entornos de desarrollo personalizados y consistentes para cada proyecto. Esto es especialmente útil cuando se trabaja en equipo o se manejan múltiples proyectos con requisitos técnicos distintos. Existen varias formas de adaptar el entorno de tu codespace a tus necesidades y preferencias, ya sea a nivel de proyecto o a nivel de usuario.
## Configuración del contenedor de desarrollo (devcontainer.json)
La forma más robusta de personalizar un codespace es mediante la configuración de contenedores de desarrollo. Esto se logra añadiendo una carpeta .devcontainer/ dentro del repositorio, con uno o más archivos de configuración, principalmente devcontainer.json.  
Esto permite definir de forma explícita:
- El sistema operativo base (imagen de contenedor)
- Las herramientas, bibliotecas o lenguajes a instalar automáticamente
- Extensiones de Visual Studio Code a incluir
- Comandos de instalación o configuración que se ejecutan al iniciar el entorno
- Variables de entorno y ajustes específicos del proyecto
## Uso de Dotfiles
Además de configurar el entorno del proyecto, los usuarios pueden personalizar su codespace de forma individual utilizando dotfiles. GitHub permite enlazar un repositorio público de dotfiles en tu cuenta, que se aplicará automáticamente a cualquier codespace que crees.
Los dotfiles permiten:
- Configurar preferencias de shell (.bashrc, .zshrc)
- Definir alias y funciones personalizadas
- Instalar herramientas o configuraciones propias
- Aplicar ajustes de Git, como nombre de usuario, editor predeterminado, etc.  
Puedes configurar esto desde tu perfil de GitHub, en la sección Codespaces > Dotfiles, y GitHub se encargará de clonar y aplicar el repositorio cada vez que inicies un nuevo codespace.
## Sincronización de configuración de VS Code
Si usas Visual Studio Code, también puedes activar la sincronización de configuración para mantener tu experiencia uniforme entre tu instalación local y los codespaces. Esta función sincroniza:  
- Temas y apariencia
- Atajos de teclado
- Fragmentos de código (snippets)
- Configuración del editor (settings.json)
- Extensiones instaladas  
Esto es especialmente útil si trabajas desde diferentes dispositivos o accedes a Codespaces desde el navegador, ya que te sentirás como si estuvieras trabajando en tu equipo local.

# Facturación y uso de Codespaces
- Cuentas personales
Todas las cuentas personales en GitHub, ya sean del plan Gratuito o Pro, incluyen una cuota mensual de uso gratuito de GitHub Codespaces. Puedes comenzar a usar esta función sin necesidad de configurar nada adicional ni proporcionar información de pago.  
Si creas un codespace desde un repositorio que pertenece a una organización, el consumo puede facturarse directamente a la organización si esta lo permite. En caso contrario, el uso se cobrará a tu cuenta personal. Una vez que superas el uso gratuito mensual, puedes continuar utilizando Codespaces agregando un método de pago y configurando un límite de gasto en tu cuenta.

- Organizaciones y empresas
Las organizaciones con planes GitHub Team o GitHub Enterprise pueden cubrir los costos de GitHub Codespaces para sus miembros y colaboradores. Esto se aplica específicamente a los codespaces creados a partir de repositorios propiedad de la organización.  
Cuando un codespace es facturado a la organización, esta se convierte en su propietaria y tiene la capacidad de eliminarlo si lo considera necesario. Además, las organizaciones pueden establecer límites de gasto y decidir quién es responsable de los pagos. La posibilidad de crear codespaces desde un repositorio de la organización puede depender de la visibilidad del repositorio y de la configuración establecida por la propia organización o empresa matriz.

# Casos de uso prácticos de GitHub Codespaces
GitHub Codespaces no solo agiliza la configuración del entorno, sino que abre posibilidades para escenarios de trabajo que antes requerían mucho tiempo o infraestructura adicional. A continuación encontrarás ejemplos de cómo aprovechar Codespaces en distintas situaciones reales:
1. Revisión rápida de Pull Requests:  
Al recibir una pull request, puedes abrir un codespace directamente desde esa rama para revisar, probar y depurar los cambios en un entorno aislado. Esto elimina la necesidad de clonar el repositorio, cambiar de rama o instalar dependencias localmente.
2. Onboarding de nuevos desarrolladores:  
Los nuevos miembros del equipo pueden empezar a trabajar de inmediato sin preocuparse por configurar el entorno de desarrollo. Con un codespace preconfigurado, todo está listo: lenguajes, dependencias, extensiones y configuraciones específicas del proyecto.
3. Contribuciones a proyectos open source:  
Los contribuidores externos pueden usar Codespaces para explorar, editar y probar proyectos open source sin necesidad de clonar el repositorio en su máquina local. Esto es ideal para quienes quieren aportar sin modificar su entorno local.
4. Pruebas en entornos aislados:  
Al crear un codespace, puedes replicar entornos de producción o testing sin afectar tu configuración local. Esto es útil para ejecutar pruebas específicas, depurar errores o verificar compatibilidades en diferentes versiones.
5. Desarrollo desde cualquier lugar:  
Como Codespaces se ejecuta en la nube y está disponible desde el navegador o VS Code, puedes continuar tu trabajo desde cualquier dispositivo con conexión a Internet, sin depender de tu equipo habitual.
6. Trabajo con múltiples proyectos:  
Si trabajas en diferentes proyectos con stacks distintos, puedes crear un codespace personalizado para cada uno. Esto evita conflictos de versiones de dependencias y mantiene tu entorno local limpio.