# Blanketfordeler Servicebus miljø konfiguration


## Generelt for at tilgå og opdatere konfigurationer

1. Gå til Service Bus Consollen: http://\<HOSTNAME\>:7001/servicebus/
2. Klik på *Create* for at starte en ny "Session"
3. Udfør ændringerne.
4. Tryk på *Close*

### Generel Miljø konfiguration
For at sikre servicebussen benytter de korrekte værdier, skal det sikres at servicebussen afspejler det miljø som den kører på.

- Gå til  *All Projects -> IntegrationsRessourser -> Resources -> Environment*
- Tilpas domain specifik værdi i tabellen: 
      - **Environment (under DomainValue) sættes til en af disse værdier (TST / SIT / TFE / PRD)** 

### Fejlrapportering
#### ITSM
4. I træstrukturen, gå til *All Projects -> FejlrapporteringsFlow -> Behandl -> FejlrapporteringITSM*
	5. Klik på *Transport* fanen
	6. Tilret URLs, således at den URL der står der, peger på Remedy ITSM i det miljø du installerer i. URLer:  
		- Remedy ITSM produktion http://172.20.248.41:6024/arsys/services/ARService?server=rdybrokerprod01&webService=Skat_Vendor_ITSM_Integration
		- Remedy ITSM test http://172.20.248.40:6024/arsys/services/ARService?server=rdybrokertest01&webService=Skat_Vendor_ITSM_Integration

#### AdminSite
10. Gå til  *All Projects -> FejlrapporteringsFlow -> Resources -> FejlrapporteringDomainValues*
	11. Tilpas domain specifikke værdier i tabellen: 
		 - **AdminSiteURLer**    	
		 - Url TST:   https://bf-adminsite.tst.ccta.dk
		 - Url SIT:   https://bf-adminsite.sit.ccta.dk
		 - URL TFE:   https://bf-adminsite.tfe.ccta.dk
		 - Url PROD:  https://bf-adminsite.ccta.dk

		- **Environment sættes til en af disse værdier (TST / SIT / TFE / PRD) og skal matche værdien for Environment under Generel Miljø konfiguration**
		
		
		

Nu skal der tilrettes til miljøet:

1. I træstrukturen, gå til *All Projects -> KundeoverblikIntegration -> Behandl -> Kundeoverblik*
	2. Klik på *Transport* fanen
	3. Tilret URLs, således at den URL der står der, peger på Kunderoverblik i det miljø du installerer i. URLer:  
		- Kunderoverblik produktion http://172.20.251.129:8081/arsys01/services/ARService?server=kob-prod&webService=KOB_Blanket
		- Kunderoverblik test http://172.20.250.211:8080/arsys/services/ARService?server=kob-test&webService=KOB_Blanket

7. I træstrukturen, gå til *All Projects -> Datawarehouseintegration -> Behandl -> StyretFilOverfoerselModtagAnmod*
	8. Klik på *Transport* fanen
	9. Tilret URIs, således at den URL der står der, peger på DW i det miljø du installerer i. URLer:  
		- DW PROD:  http://172.20.242.43:7333/StyretFiloverfoerselModtagAnmodService
		- DW TFE:   http://172.20.242.127:7333/StyretFiloverfoerselModtagAnmodService
	 
     - **Environment sættes til en af disse værdier (TST / SIT / TFE / PRD)**
   
12. Gå til  *All Projects -> IntegrationsRessourser  -> Resources -> Environment*
13. Tilpas domain specifik værdi i tabellen: 
    
      - **Environment (under DomainValue) sættes til en af disse værdier (TST / SIT / TFE / PRD)** 
   
14. Afslut import og tilrettelser ved at trykke på *Activate* knappen og efterfølgende på *Activate* knappen i *Confirm Session Activation*
