# Lern-Bericht
Maria Soldo

## Einleitung
In diesem Modul ging um Applikaitonssicherheiten zu implementieren. In diesem Lernbericht werde ich die Sicherheitslücke "Open Redirect" vorstellen.

## Was habe ich gelernt?
Ich habe gelernt, was "Open Redirect " ist und wie man die Applikation davor schützen kann.

## Beschreibung
Folgendes habe ich gelerent:

* Was Open Redirect ist und was die Risiken davon sind:
Open Redirect ist wenn die Applikation eine unvalidierte URL erhält und den User mit der unvalidierten URL weiterleitet. Das kann zum Risiko, phishing-attacken führen.

* Wie man die Appliaktion schützen kann:
```Java
   public void back() {
        FacesContext context = FacesContext.getCurrentInstance();
        HttpServletResponse response = (HttpServletResponse) context.getExternalContext().getResponse();
        //Die "Wurzel" der Url die benutzt werden soll
        String baseUrl = "http://localhost:8080/SSA-5/";
        if (!redirectionUrl.startsWith(baseUrl)) {
            //Wenn die Url die weitergeleitet werden muss, mit der baseUrl anfängt dann soll:
            try {
                //es zur angehängten "index.xhtml" weitergeleitet werden. 
                response.sendRedirect(redirectionUrl = baseUrl + "/secured/index.xhtml");
            } catch (IOException ex) {
                Logger.getLogger(NewsController.class.getName()).log(Level.SEVERE, null, ex);
            }
        }
    }
```

* Was für einen grossen Unterschied der Schutz machen kann:

[![Watch the video](https://img.youtube.com/vi/GRQmvTj9dOc/default.jpg)](https://youtu.be/GRQmvTj9dOc)

## Verifikation
Mit der Defention und dem Code-Auschnitt, zeige ich das ich das Risiko und die Implentation verstanden habe. Das Video soll die Gefahr und den Schutzt zeigen.

# Reflektion zum Arbeitsprozess

👍 Ich konnte das Open Redirect repetieren und verstehe es auch recht gut.

👎 Das Repetieren dauerte etwas länger als gedacht, weil ich fast alles vergessen habe.

**VBV**: ✍️ Eventuel, während den Aufgaben lösen eine Aufnahme machen, um diese später wieder anzuschauen.
