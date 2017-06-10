# vivifyproba
package vivifyproba;

import java.util.GregorianCalendar;
import java.util.LinkedList;
import tipovi_pregleda.*;
/**
 *
 * 
 */
public class Doktor {
    private String ime;
    private String prezime;
    private String specijalnost;
    private int doktorid;
    private LinkedList<Pacijent> listaPacijenata;
   
   
    public Doktor() {}
    public Doktor(String ime, String prezime, String specijalnost, int doktorid) {
        this.ime = ime;
        this.prezime = prezime;
        this.specijalnost = specijalnost;
        this.doktorid = doktorid;
    }
    
    public String getIme() {
        return ime;
    }
    public void setIme(String ime) {
        this.ime = ime;
    }
    public String getPrezime() {
        return prezime;
    }
    public void setPrezime(String prezime) {
        this.prezime = prezime;
    }
    public String getSpecijalnost() {
        return specijalnost;
    }
    public void setSpecijalnost(String specijalnost) {
        this.specijalnost = specijalnost;
    }
    public int getDoktorID() {
        return doktorid;
    }
    public void setDoktorID(int doktorid) {
        this.doktorid = doktorid;
    }
    public void zakazivanjePregleda(GregorianCalendar datumIVreme, String tipPregleda, Pacijent pacijent) {
        if(tipPregleda.equals("pritisak")) {
            PregledKrvnogPritiska pre = new PregledKrvnogPritiska(datumIVreme, pacijent, this);
        } else if(tipPregleda.equals("secer")) {
            PregledSecera pre = new PregledSecera(datumIVreme, pacijent, this);
        } else if(tipPregleda.equals("holesterol")) {
            PregledHolesterola pre = new PregledHolesterola(datumIVreme, pacijent, this);
        }
    }
    public void obavljanjePregleda() {
        
    }
    
}
