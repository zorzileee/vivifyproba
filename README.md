# vivifyproba

package tipovi_pregleda;

import java.util.GregorianCalendar;
import vivifyproba.Doktor;
import vivifyproba.Pacijent;

/**
 *
 * @author Gabi
 */
public abstract class Pregled {
    protected GregorianCalendar zakazano;
    protected Pacijent p;
    protected Doktor d;
    
    public abstract void zakazivanjePregleda(GregorianCalendar gc, Pacijent p, Doktor d);
    
}
