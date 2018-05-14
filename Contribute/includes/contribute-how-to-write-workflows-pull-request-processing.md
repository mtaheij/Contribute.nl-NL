## <a name="pull-request-processing"></a>Verwerking van pull-aanvragen

In de vorige sectie werd uitgelegd hoe u voorgestelde wijzigingen kunt indienen door deze in een nieuwe pull-aanvraag te bundelen die wordt toegevoegd aan de wachtrij voor pull-aanvragen in de doelopslagplaats. Met een pull-aanvraag wordt het samenwerkingsmodel van GitHub ingeschakeld door de wijzigingen uit uw werkvertakking te 'trekken' (pull) en samen te voegen met een andere vertakking. Die andere vertakking is meestal de standaard 'hoofdvertakking' in de hoofdopslagplaats.

### <a name="validation"></a>Validatie

Voordat uw pull-aanvraag kan worden samengevoegd met de doelvertakking, moeten er misschien één of meer pull-aanvraagvalidaties worden uitgevoerd. Validaties kunnen verschillend zijn, afhankelijk van de omvang van voorgestelde wijzigingen en de regels van de doelopslagplaats. Nadat uw pull-aanvraag is ingediend, kunnen er één of meer van de volgende dingen gebeuren:

- **Samenvoegbaarheid:** Er wordt eerst een GitHub-basistest voor samenvoegbaarheid uitgevoerd om te controleren of de voorgestelde wijzigingen in uw vertakking conflicteren met de doelvertakking. Als de pull-aanvraag aangeeft dat dit inderdaad het geval is, moet u de inhoud die het samenvoegingsconflict veroorzaakt, afstemmen voordat de verwerking kan worden hervat.
- **CLA:** Als u bijdraagt aan een openbare opslagplaats en geen Microsoft-werknemer bent, wordt u afhankelijk van de omvang van de voorgestelde wijzigingen misschien gevraagd een korte CLA (Contribution License Agreement) in te vullen wanneer u voor het eerst een pull-aanvraag bij deze opslagplaats indient. Nadat de CLA-stap is goedgekeurd, wordt uw pull-aanvraag verwerkt.
- **Labeling:** Er worden automatisch labels op uw pull-aanvraag toegepast om de status van uw pull-aanvraag aan te geven terwijl deze de validatiewerkstroom doorloopt. Nieuwe pull-aanvragen kunnen bijvoorbeeld automatisch het label 'niet-samenvoegen' krijgen, wat aangeeft dat de pull-aanvraag de stappen voor validatie, controle en goedkeuring nog niet heeft doorlopen.
- **Validatie en build:** Uw wijzigingen worden door geautomatiseerde controles onderzocht om te controleren of ze de validatietests doorstaan. De validatietests kunnen waarschuwingen of fouten opleveren, waardoor u één of meer bestanden in uw pull-aanvraag moet wijzigen voordat deze kan worden samengevoegd. De resultaten van de validatietests worden als een opmerking in uw pull-aanvraag toegevoegd, zodat u deze kunt controleren, en kunnen ook per e-mail naar u worden gestuurd.
- **Fasering:** De artikelpagina’s die worden beïnvloed door uw wijzigingen, kunnen automatisch in een faseringsomgeving worden geïmplementeerd voor controle na een succesvolle validatie en build. Voorbeeld-URL’s worden in een pull-aanvraagopmerking weergegeven.
- **Automatische samenvoeging:** De pull-aanvraag kan automatisch worden samengevoegd als deze de validatietests doorstaat en aan bepaalde criteria voldoet. In dat geval hoeft u verder niets meer te doen.

### <a name="review-and-sign-off"></a>Controle en goedkeuring

Nadat de pull-aanvraagverwerking is voltooid, moet u de resultaten (pull-aanvraagopmerkingen, voorbeeld-URL’s enz.) controleren om te bepalen of de bestanden ervan nog verder moeten worden gewijzigd voordat u de pull-aanvraag goedkeurt voor samenvoeging. Als een revisor voor pull-aanvragen uw pull-aanvraag heeft gecontroleerd, geeft deze misschien ook feedback via opmerkingen als er uitstaande problemen/vragen zijn die moeten worden opgelost voordat de pull-aanvraag wordt samengevoegd.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Als de pull-aanvraag probleemvrij en goedgekeurd is, worden uw wijzigingen weer samengevoegd met de bovenliggende vertakking en wordt de pull-aanvraag gesloten.

### <a name="publishing"></a>Publicatie

Vergeet niet dat uw pull-aanvraag moet worden samengevoegd door een revisor voor pull-aanvragen voordat de wijzigingen kunnen worden opgenomen in de volgende geplande publicatie. Pull-aanvragen worden gewoonlijk gecontroleerd/samengevoegd in de volgorde waarin deze zijn ingediend. Als uw pull-aanvraag moet worden samengevoegd voor een bepaalde publicatie, moet u van tevoren met uw revisor voor pull-aanvragen overleggen en samenwerken om ervoor te zorgen dat de samenvoeging vóór de publicatie plaatsvindt.

Nadat uw bijdragen zijn goedgekeurd en samengevoegd, worden ze opgepikt door het Docs.Microsoft.Com-publicatieproces. Publicatiemomenten kunnen variëren, afhankelijk van het team dat de opslagplaats beheert waaraan u bijdraagt. Artikelen die onder de volgende paden worden gepubliceerd, worden gewoonlijk maandag t/m vrijdag om ongeveer 10:30 uur en 15:30 uur Pacific Time geïmplementeerd:

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Het kan tot 45 minuten duren voordat artikelen online verschijnen nadat ze zijn gepubliceerd. Nadat uw artikel is gepubliceerd, kunt u uw wijzigingen controleren via de desbetreffende URL: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
