cagatay civici cerado r de primefaces
Maven
Ejb
jpa
jsf+primefaces
Nuevoproyecto->maven->webapplicaiotn
		package controller
		servidor aplicadiones cdi
Añadimos framesork jsf
---Maven gestionador de librerias y dependencias---
--patron facade

@Entity
@Table(name="categoria")
@Id
@GeneratedValue8startegy = GenerationYpe:IDNTITY)
@GeneratedValue

Creando ejb para jpa
Patron fachada
		se accede a los metodos por una interface
	Clase abstracta
		Objeto generico (cualquier tipo de objeto)
 		las clases qeu lo heredan implementa los meotdos
@Column
	EntityManager //se relaciona para la interacin con la base
Controlller //parte controlador informaicon

Proceso para persistir datos
-Vista
		 input relacionado con #categoriaController.categoria.nombre//nombre propiedad del objeto categoria
		 buton relacionado con
		 #categoriaController.registarr()
		 llama controller metdo registrar
-Controller
		public void registrar(){//funcion registrar la cual es llamada desde la vista
			try{
				categoriaEJB.create(categoria);//se llama al metodo create (manadadno el objeto categoria) de Ejb el cual es una interface
			}catch(Exception e){
			//mensaje en caso de error
		}
	}
-Interface
		void create(Categoria categoria)
-Categoira facade
		-esta  extiende de Abastracfacade<categoria> e implennta Categoriafacadelocal(interface)
			- abstractfacade para interactuar ocn la base de datos
			-Categoriafacade es la interface
		-aqui se invoca al constructor
			public CategoriaFacade(){
				super(Categoria.class)//super es una herencia por lo qeu se busca al padre y se le pasa la clase categoria
-AbstractFacade 
		- contiene los metosdos qque tiene el metodo create y de esta manera persiste los datos
Resumiendo secuencia
		xhtml
		controller
		Ejb(interfaz)
		Ejb(Impl)
-Se puede usar hibernte pra crear la base de dato mapeando las clases

Link para navegacion
command link cuando tiene logica
match (propiedad para ver si las dos claves osn iguales)

//Stack de tecnologias pra tesis
Eclipse 
	Ver diferencai entre netbenas y eclipse y deci r por q se escojio eclipse
Maven
	Enumerar diferenets gestores de dependencais y porq se esojio maven vs gradle
Hibernate
	Porq se lo eligio como orm y como se crean las tablas en la base de datos desde el codigo en java
Postgress
	Comparacion con las distintas vaces de datoc mo mysql sqlserver y mas y por q se escojio dicha base de datos pra el desarrollo
Primefaces
	Framework jsf porq se escojio y en qeu ayuda a als vsitas y diferenccia entre otros framework como icefaces y ams
Notas segundo tutoriales primefaces

Orm
	object relation mapping
	Mapeador de realciones de objetos
Impedancia
	divorciadado totalmente de la programacion orintada a bojetos
JDBC
	Obligados atrapar la excepcion que se puede dar
		Base de datos no disponible
Disminuyendo la impedanci a traves dle mapeo
	@Entity
	para declarra un entidad
	JPA
		Java persistence API
Hibernate
	alineo con el standar
Jpa
	es una api estandar como jdbc
SErvidor aplicaciones
	ya vienen las librerais de hibernate
Tomcat 
	solo tiene las librerias para correr
Maven
	Es un gestor de proyectos
	se declaran las dependencias en un pom.xml
maven update proyect para poder actualiar el poryecto
-----------
1.- rebizar como configurar el pon.xml
Hibernate Implementacion
	se realizan las consultas sobre los objetos
	jpa es la interface e hibernate la implementan
MVC
	JPA es mas para le modelo
	Vista que ve es usuairo
	Controlador recibe comco el usuarioi interactua con la vista
Servlets
	son la base pra los get y post
Primero 
	todo era servlets
Sgundo 
	se invito jsp (pagians html con codigo java)
Jstl
	Java astarndar tag library: para poder hacer menos codigo dentro de la pagina
C
	controlador
		sepuede usar patrones DAO(Para parte de persisitencia)
MVC Frameworks
 
Porque usar jsf?
	implementa mvc
Persistence.xml
	se indica cual es nombre de una unidad de persistencia
	<persistence-unit name="default">
	</persistence-unit>
jdni
	es como poner un sigla a una conexion en un serdiro de aplicacones
automatizar la creacion y actualizacion de tablas
	create-drop: las tabals con creads por el mismo Hibernate y luego eliminadas al final de la ejecucion del programa
	update: nada es eliminado , solo se actualiza o crea algo nuevo , se mantiene todos los datos. Util para aplicaciones que estan en produccion y que nada puede ser descartado
	validate:
jpql 
	es una seleccion al bojeto no a las tablas
jpql
	puede utilizar funciones
		abs
		sqrt
		current_timestamp
		avg
		max
		min
		count
--- consultas ocn jpql
jsf y Jpa
lenguaje jpql
	
	@NamedQuery(nam="Automovel.listarTodos",
		query="select a form Atumovil a")
Lazy, n+1

tenemos en la vista
	exception
		LazyInitializationException
orm
	no nos libera de la performance
lazy a igger si es posible
igger a lazy no es posible

Ver q es patorn DAO
	Bean validation y JPA
Hibernate validation
	auto
BeanValidation y Jsf es automatica 
BeanValidation y Jpa tambien es automatica

jsf es el framwrok mvc de java es otra api
cambiar trrjet para cambair la versin en la que trabaja maven

ver como configurar persistence.xml
como configurar pom.xml con maven

jpa util es una buen practica
	ver codigo javaee7 en github para ver si se peudo correr con hibernate
ver hola mundo con hibernate
Creacino de app con netbeans
	deploy para grabae
Dinamic web proeyct
	tiene un problema de que se encutnra vinculado 
	por lo cual se usa maven para que se peuda usar en cualquier computadora
	y sin depender del IDe
Proyecto ocn maven es mucho mejor para le manejo de dependencias
war proyecto pra un web
	src/main/java
		codigo java
	src/main/resource
		codigo que no es java
maven 
	pom.xml
		se puede especificar el encondign UTF-8
	web dinamic 3.0
		es desde donde es opcional el web.xml
maven 
	se puede trabajr con cualquierea de los ides

Servlet es aquel q  se encarga de recibir las peticiones

maven igual permite añadir jars
	<dependency>
		<groupId>javax.servlet</groupId>
	</dependency>
scope
	servlet
		es proveido por el servidor de aplicacones
		se lo marca como provider cuando esto se da el servido rde aplicaciones
ctrl+shift+o
	para realziar una importacion rapida
para que valga con tomcat
	primero confiturar si esta con java 1.7
en web content es donde se crea los jsp
se pueden añadir librerias que tiene el servidor
	
Debug es cuando se desea que para en un puntto para debuggerar
	debug es el que me permtie ver las variables y ver si hahay algun eerro ren el codigo
Uso de jax-rs

MOjarra
	implementacin mas conocida de jsf
Controladores
	BeanManejados
		administrados por java server face
no se tiene q declarra en ningun lado la vista con el co ntrolador q por convencion la vista usa los bean
	clases
		Empienzan con mayuscula siguen camelCase
	vistas
		empiezan con miniscula siguen camelcase

@ManagedBean
	Es es que se encarga de unir la vista con el controlador (bean)
h html
ui para usar repeats
	ui:repeat var = "nombre" value= "{}"
@RequestScoped
	se vuelve hacer el request cada vez y se ponen por defecto
@ViewScoped
	solo mantiene mientras se esta en la vista lo que se va añadiendo pero cuando se va otra se pierde ocmpletamente
@SessionScoped
	que no pierda la sesion y q mantega guardado los datos
	tiene un timepo limitado
	
