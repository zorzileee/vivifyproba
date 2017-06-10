# vivifyproba
package tipovi_pregleda;

import java.util.GregorianCalendar;
import vivifyproba.*;
/**
 *
 * @author Gabi
 */
public class PregledKrvnogPritiska extends Pregled {
    private int puls;
    private int gornjaGranica;
    private int donjaGranica;
    
    // hmmm, mislim da su u pitanju celi brojevi, ( 300 sa 200 ) , 85 otkucaja u minutu za puls npr.

    @Override
    public void zakazivanjePregleda(GregorianCalendar gc, Pacijent p, Doktor d) {
       this.zakazano = gc;
       this.p = p;
       this.d = d;
    }

    public PregledKrvnogPritiska(GregorianCalendar gc, Pacijent p, Doktor d) {
        zakazivanjePregleda(gc, p, d);
    }
    
    
    
    
    public int getPuls() {
        return puls;
    }
    public void setPuls(int puls) {
        this.puls = puls;
    }
    public int getGornju() {
        return gornjaGranica;
    }
    public void setGornju(int gornja) {
        this.gornjaGranica = gornja;
    }
    public int getDonja() {
        return donjaGranica;
    }
    public void setDonja(int donja) {
        this.donjaGranica = donja;
    }
}
