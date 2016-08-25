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