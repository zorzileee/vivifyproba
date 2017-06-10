# vivifyproba

package tipovi_pregleda;

import java.util.GregorianCalendar;
import vivifyproba.*;
/**
 *
 *
 */
public class PregledSecera extends Pregled {
    
    private double nivoSecera;
    private GregorianCalendar poslednjiObrok;
    

    public PregledSecera(GregorianCalendar gc, Pacijent p, Doktor d) {
        zakazivanjePregleda(gc,p,d);
        
    }
    
    
    @Override
    public void zakazivanjePregleda(GregorianCalendar gc, Pacijent p, Doktor d) {
        this.zakazano = gc;
         this.p = p;
       this.d = d;
    }
    
    public double getNivo() {
        return nivoSecera;
    }
    public void setNivo(double nivoSecera) {
        this.nivoSecera = nivoSecera;
    }
    public GregorianCalendar getVremePoslednjeg() {
        return poslednjiObrok;
    }
    public void setVremePoslednjeg(GregorianCalendar gc) {
        this.poslednjiObrok = gc;
    }
}
