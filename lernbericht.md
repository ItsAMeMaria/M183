# Lern-Bericht
Maria Soldo

## Einleitung
In diesem Modul ging um Applikaitonssicherheiten zu implementieren. In diesem Lernbericht werde ich die Sicherheitslücke "Open Redirecting" vorstellen.

## Was habe ich gelernt?
Ich habe gelernt, was "Open Redirecting " ist und wie man die Applikation davor schützen kann.

## Beschreibung

✍️ Verwenden Sie drei verschiedene Medien, um zu zeigen, was Sie gelernt haben. Zum Beispiel:
Folgendes habe ich gelerent:

* Was Open Redirecting ist und was die Risiken davon sind:

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

✍️ Erklären Sie kurz und bündig, inwiefern die von Ihnen verwendeten Medien zeigen, was Sie gelernt haben.
* Mit der Defention und dem Code-Auschnitt, zeige ich das es 

# Reflektion zum Arbeitsprozess

👍 Ich konnte das Open Redirect repetieren und verstehe es auch recht gut.

👎 Das Repetieren dauerte etwas länger als gedacht, weil ich fast alles vergessen habe.

**VBV**: ✍️ Eventuel, während den Aufgaben lösen eine Aufnahme machen, um diese später wieder anzuschauen.
