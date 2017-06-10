# vivifyproba

package vivifyproba;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.LinkedList;

/**
 *
 * @author Gabi
 */

public class Test {
    private static LinkedList<Doktor> listaDoktora = null;
    
    static BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
    public static Doktor getDok(int doktorid) {
        for(Doktor d : listaDoktora) {
            if(d.getDoktorID() == doktorid) return d;
        }
        return null;
    }
    public static int odabirDoktora(Pacijent p) {
        int s = 0;
        for(Doktor d : listaDoktora) {
            System.out.println(d.getDoktorID());
        }
        try {
            s = Integer.parseInt(in.readLine());
            p.setDoktor(getDok(s));
        } catch(Exception e) {
             e.printStackTrace();
        }
        return s;
    }
    
    public static void main(String[] arguments) {
        Pacijent p1 = new Pacijent("Zoran","Sovrlic",220799575, 1583);
        Doktor d1 = new Doktor("Marko", "Maric", "kardio-hirurg", 53);
        listaDoktora.add(d1);
        odabirDoktora(p1);
        d1.zakazivanjePregleda(new GregorianCalendar(), "secer", p1);
        d1.zakazivanjePregleda(new GregorianCalendar(), "pritisak", p1);
        d1.obavljanjePregleda();
        d1.obavljanjePregleda();
    }
}
