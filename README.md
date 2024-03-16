//# luis-miguel-moreno-potes
//parcial del estudiante luis miguel moreno potes
//programado por luis miguel moreno potes
public class Libro {
    protected String titulo;
    protected String autor;
    protected String propietario;
    protected double precio;
    
    public Libro(String titulo, String autor, String propietario, double precio) {
        this.titulo = titulo;
        this.autor = autor;
        this.propietario = propietario;
        this.precio = precio;
    }

    public String getTitulo() {
        return titulo;
    }

    public void setTitulo(String titulo) {
        this.titulo = titulo;
    }

    public String getAutor() {
        return autor;
    }

    public void setAutor(String autor) {
        this.autor = autor;
    }

    public String getPropietario() {
        return propietario;
    }

    public void setPropietario(String propietario) {
        this.propietario = propietario;
    }

    public double getPrecio() {
        return precio;
    }

    public void setPrecio(double precio) {
        this.precio = precio;
    }

    public void imprimir(){
        System.out.println("el titulo es: " + titulo );
        System.out.println(" el autor es: " + autor);
        System.out.println("el propietario es: " + propietario);
        System.out.println("el precio del libro es:  " + precio);
    }


}
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
public class LibrosDeTexto extends Libro{
    private String curso;
    
    

    public LibrosDeTexto(String titulo, String autor, String propietario, double precio, String curso) {
        super(titulo, autor, propietario, precio);
        //TODO Auto-generated constructor stub
        this.curso = curso;
    }

    public String getCurso() {
        return curso;
    }
    
    
    public void setCurso(String curso) {
        this.curso = curso;
    }
    





    public void ImprimirAqui1(){
        super.imprimir();
        System.out.println("el curso es: " + curso);
    }

}
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
public class LibroDeTextoInstitucion extends LibrosDeTexto {
    private String facultad;
    public LibroDeTextoInstitucion(String titulo, String autor, String propietario, double precio, String curso,String facultad) {
        super(titulo, autor, propietario, precio, curso);
        //TODO Auto-generated constructor stub
        this.facultad = facultad;
    }


    public String getFacultad() {
        return facultad;
    }
    
    
    public void setFacultad(String facultad) {
        this.facultad = facultad;
    }

    public void imprimirAqui2(){
        super.imprimir();
        System.out.println("la facultad es: " + facultad);
    }
    
}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
public class Novelas  extends LibroDeTextoInstitucion{
    private String tiposNovelas;

    public Novelas(String titulo, String autor, String propietario, double precio, String curso, String facultad, String tipoNovelas) {
        super(titulo, autor, propietario, precio, curso, facultad);
        //TODO Auto-generated constructor stub
        this.tiposNovelas = tipoNovelas;
    }


    public String getTiposNovelas() {
        return tiposNovelas;
    }

    public void setTiposNovelas(String tiposNovelas) {
        this.tiposNovelas = tiposNovelas;
    }

    public void imprimirAqui3(){
        super.imprimir();
        System.out.println(" el tipo de novela es: " + tiposNovelas);
    }

}
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
public class main {
    public static void main(String[] args) {
        
        Libro libro1 = new Libro(null, null, null, 0);
        libro1.setTitulo(" Griffonia ");
        libro1.setAutor("Michael Peinkofer ");
        libro1.setPropietario(" luis");
        libro1.setPrecio(45000);
        libro1.imprimir();

        System.out.println("----------------------------------------------------------------");

        LibrosDeTexto libro2 = new LibrosDeTexto(null, null, null, 0, null);
        libro2.setTitulo(" dragon ball ");
        libro2.setAutor("akira toriyama ");
        libro2.setPropietario(" luis");
        libro2.setPrecio(56000);
        libro2.setCurso(" A12");
        libro2.ImprimirAqui1();
        System.out.println("----------------------------------------------------------------");

        LibroDeTextoInstitucion libro3 = new LibroDeTextoInstitucion(null, null, null, 0, null, null);
        libro3.setTitulo(" el caballero de la armadura oxidada ");
        libro3.setAutor(" Robert fisher ");
        libro3.setPropietario(" miguel");
        libro3.setPrecio(15000);
        libro3.setFacultad("fantastico");
        libro3.imprimirAqui2();
        System.out.println("----------------------------------------------------------------");

        Novelas libro4 = new Novelas(null, null, null, 0, null, null, null);
        libro4.setTitulo(" naruto ");
        libro4.setAutor(" gideo ");
        libro4.setPropietario(" don luis");
        libro4.setPrecio(73000);
        libro4.setTiposNovelas(" anime");
        libro4.imprimir();

    }
    
}

