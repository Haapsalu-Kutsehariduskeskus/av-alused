
# Arvutivõrkude alused (3 EKAP) - Õpilase juhend

Tere tulemast **Arvutivõrkude alused** kursusele! Selles juhendis saad teada, kuidas kasutada nii **Google Classroomi** kui ka **GitHub Classroomi**, et täita ülesandeid, laboreid ja olla kursuse tegevustega kursis.

---

## Kuidas kasutada Google Classroomit

Kasutame **Google Classroomit** üldiseks suhtluseks, teadete jagamiseks ja õppematerjalide, nagu slaidid, videod ja muud ressursid, jagamiseks.

### Google Classroomi kasutamise sammud:
1. **Logi sisse**: Ava **Google Classroom** oma kooli e-posti kaudu (nt `sinunimi@hkhk.edu.ee`).
2. **Kontrolli teateid**: Vaata olulisi värskendusi kursuse, tähtaegade ja uute ülesannete kohta.
3. **Leia ülesannete lingid**: Iga nädal postitatakse **Google Classroomi** alla **Classwork** uus **GitHub Classroomi ülesande link**.
4. **Juurdepääs õppematerjalidele**: Kõik slaidid, lugemismaterjalid ja lisamaterjalid postitatakse ka sinna.

**Oluline**: Kontrolli regulaarselt Google Classroomi, et saada teada uusi teateid ja ülesannete linke.

---

## Kuidas kasutada GitHub Classroomit

Kasutame **GitHub Classroomit** kõigi tehniliste ülesannete jaoks, sealhulgas laborid, kodutööd ja lõpuprojekt.

### GitHub Classroomi kasutamise sammud:
1. **Liitu ülesandega**:
   - Google Classroomis klõpsa **GitHub Classroomi lingile** vastava nädala ülesande jaoks.
   - See link loob sulle **privaatse GitHubi repote**, kus saad oma tööd teha.

2. **Klooni repo**:
   - Kui ülesande repo on loodud, **klooni** see oma arvutisse kasutades Git käske või GitHub Desktopi:
     ```
     git clone https://github.com/[sinu-kasutajanimi]/[ülesande-repo-nimi]
     ```

3. **Tee ülesanne ära**:
   - Täida labor või ülesanne vastavalt juhistele.
   - Salvesta oma töö, tehes **commitid** lokaalselt:
     ```
     git add .
     git commit -m "Täidetud 1. nädala lab"
     ```

4. **Pushi oma töö GitHubi**:
   - Kui töö on tehtud, **pushi** muudatused GitHubi:
     ```
     git push origin main
     ```

5. **Esita oma töö**:
   - Sinu töö saab automaatselt õppejõule nähtavaks, kui see on GitHubi üles laetud.
   - **Kui nõutud**, tee **pull request** või vasta igale tagasisidele kasutades repo **issues** sektsiooni.

---

## Workglow näide:

1. **1. samm**: Kontrolli Google Classroomist ülesande linki.
2. **2. samm**: Klõpsa GitHub Classroomi linki ja loo oma privaatne repo.
3. **3. samm**: Klooni repo ja tee ülesanne oma arvutis.
4. **4. samm**: Pushi muudatused GitHubi, kui töö on valmis.
5. **5. samm**: Vaata üle õppejõu tagasiside repost või pull requestidest/issues sektsioonist.

---

## Olulised meeldetuletused:

- **Tähtajad**: Kontrolli iga ülesande tähtaegu nii Google Classroomis kui ka GitHub Classroomis.
- **Abi ja küsimused**: Kui vajad abi mõne ülesandega, postita küsimus oma GitHubi repo **Issues** sektsiooni või Google Classroomi **Discussions** ossa.
- **Koostöö**: Aruta probleeme kaasõpilastega, kuid kõik esitatav töö peab olema sinu enda tehtud.
- **Hilinenud esitused**: Hilinenud töö võib saada miinuspunkte, kui õppejõud ei ole pikendust andnud.

---

### Abi vajate?

Kui teil on probleeme GitHub Classroomi või Google Classroomi kasutamisega, ärge kartke ühendust võtta **Google Classroomi Discussions** sektsioonis või saata e-kiri aadressil **[maria.talvik@hkhk.edu.ee]**.
