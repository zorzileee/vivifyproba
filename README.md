# vivifyproba
package tipovi_pregleda;

import java.util.GregorianCalendar;
import vivifyproba.*;
/**
 *
 * @author Gabi
 */
public class PregledHolesterola extends Pregled {
    private double nivoHolesterola;
    private GregorianCalendar vremePoslednjeg;

    public PregledHolesterola(GregorianCalendar zaZakazati, Pacijent p, Doktor d) {
        zakazivanjePregleda(zaZakazati, p, d);
    }

    
    
    
    @Override
    public void zakazivanjePregleda(GregorianCalendar gc, Pacijent p, Doktor d) {
        this.zakazano = gc;
    }
    public double getNivo() {
        return nivoHolesterola;
    }
    public void setNivo(double nivo) {
        this.nivoHolesterola = nivo;
    }
    public GregorianCalendar getVremePoslednjeg() {
        return vremePoslednjeg;
    }
    public void setVremePoslednjeg(GregorianCalendar gc) {
        this.vremePoslednjeg = gc;
    }
    
    
}
