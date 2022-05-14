# one.digitalinovation.gof
package one.digitalinovation.gof;

/**
 *Singleton "preguiçoso".
 *
 * @author VANIA
 */
public class Singletonlazy {
	
	private static Singletonlazy instancia;
	
	private Singletonlazy () {
		super();
	}
	public static Singletonlazy getInstacia() {
		if (instancia ==null ) {
			instancia =new Singletonlazy();
		}
		return instancia;
		}
	public static Singletonlazy getInstancia() {
		// TODO Auto-generated method stub
		return null;
	}
}
package one.digitalinovation.gof;
/**
 *Singleton "apressado".
 *
 * @author VANIA
 */
public class Singletonlazyholder {
	
	private static class instanceholder{
	private static Singletonlazyholder instancia = new Singletonlazyholder();
	}
	private Singletonlazyholder () {
		super();
	}
	public static Singletonlazyholder getInstacia() {
		return instanceholder.instancia;
		}
}
package one.digitalinovation.gof;

public class Teste {
	
	public static void main (String[] args) {
		Singletonlazy lazy = Singletonlazy.getInstancia();
		System.out.println(lazy);
		lazy= Singletonlazy.getInstancia();
		char[] holder = null;
		System.out.println(holder);
	}
}
