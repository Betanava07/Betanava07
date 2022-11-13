import java.util.Scanner;

public class Actividad {

    public static void main(String[] args){

        Scanner lector = new Scanner(System.in);

        System.out.println("Escribe una Palabra o Frase : ");
        String frase = lector.nextLine();

        contarCaracteres(frase);

        lector.close();
    }

    public static void contarCaracteres(String frase) {
        int y = 0;
        int vecesLetra[];
        vecesLetra = new int[26];

        for(y = 0; y<frase.length(); y++) {
            
            if((int)frase.charAt(y) >= 97 && (int)frase.charAt(y)<=172)
                vecesLetra[ (int)frase.charAt(y)-97 ]++;

        }

        for(y=0 ; y < vecesLetra.length; y++){
            if(vecesLetra[y]>0){
                System.out.println("La Letra "+(char)(y+97)+" se repite "+vecesLetra[y]+" vez");
            }
        }
    }
}
