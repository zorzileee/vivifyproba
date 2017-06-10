# vivifyproba

package vivifyproba;

/**
 *
 * @author
 */
public class Pacijent {
    private String ime;
    private String prezime;
    private long JMBG;
    private int brojZdravstvenog;
    
    private Doktor mojDoktor;

    public Pacijent(String ime, String prezime, long JMBG, int brojZdravstvenog) {
        this.ime = ime;
        this.prezime = prezime;
        this.JMBG = JMBG;
        this.brojZdravstvenog = brojZdravstvenog;
    }

    public Pacijent() {
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
    public long getJMBG() {
        return JMBG;
    }
    public void setJMBG(int JMBG) {
        this.JMBG = JMBG;
    }
    public int getBroj() {
        return brojZdravstvenog;
    }
    public void setBroj(int brojZdr) {
        this.brojZdravstvenog = brojZdr;
    }
    public Doktor getDoktor() {
        return mojDoktor;
    }
    public void setDoktor(Doktor d) {
        this.mojDoktor = d;
    }
    
}

