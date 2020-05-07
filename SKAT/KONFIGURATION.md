# Blanketfordeler Servicebus miljø konfiguration


## Generelt for at tilgå og opdatere konfigurationer

1. Gå til Service Bus Consollen: http://\<HOSTNAME\>:7001/servicebus/
2. Klik på *Create* for at starte en ny "Session"
3. Udfør ændringerne.
4. Tryk på *Activate* knappen i *Confirm Session Activation*

### Generel Miljø konfiguration
For at sikre servicebussen benytter de korrekte værdier, skal det sikres at servicebussen afspejler det miljø som den kører på.

- Gå til  *All Projects -> IntegrationsRessourser -> Resources -> Environment*
- Tilpas domain specifik værdi i tabellen: 
  - **Environment (under DomainValue) sættes til en af disse værdier (TST / SIT / TFE / PRD)** 

### Fejlrapportering
#### Remedy ITSM
- I træstrukturen, gå til *All Projects -> FejlrapporteringsFlow -> Behandl -> FejlrapporteringITSM*
- Klik på *Transport* fanen
- Tilret URLs, således at den URL der står der, peger på Remedy ITSM i det miljø du installerer i. URLer:  
  - Remedy ITSM produktion http://172.20.248.41:6024/arsys/services/ARService?server=rdybrokerprod01&webService=Skat_Vendor_ITSM_Integration
  - Remedy ITSM test http://172.20.248.40:6024/arsys/services/ARService?server=rdybrokertest01&webService=Skat_Vendor_ITSM_Integration

#### AdminSite
- Gå til  *All Projects -> FejlrapporteringsFlow -> Resources -> FejlrapporteringDomainValues*
- Tilpas domain specifikke værdier i tabellen: 
  - **AdminSiteURLer**    	
  - URL TST:   https://bf-adminsite.tst.ccta.dk
  - URL SIT:   https://bf-adminsite.sit.ccta.dk
  - URL TFE:   https://bf-adminsite.tfe.ccta.dk
  - URL PROD:  https://bf-adminsite.ccta.dk

  **Environment sættes til en af disse værdier (TST / SIT / TFE / PRD) og skal matche værdien for Environment under Generel Miljø konfiguration**
		
### Integration: Kundeoverblik
- I træstrukturen, gå til *All Projects -> KundeoverblikIntegration -> Behandl -> Kundeoverblik*
- Klik på *Transport* fanen
- Tilret URLs, således at den URL der står der, peger på Kunderoverblik i det miljø du installerer i. URLer:  
  - Kunderoverblik produktion http://172.20.251.129:8081/arsys01/services/ARService?server=kob-prod&webService=KOB_Blanket
  - Kunderoverblik test http://172.20.250.211:8080/arsys/services/ARService?server=kob-test&webService=KOB_Blanket

### Integration: Datawarehouse
#### Styret FilOverførsel
- I træstrukturen, gå til *All Projects -> Datawarehouseintegration -> Behandl -> StyretFilOverfoerselModtagAnmod*
- Klik på *Transport* fanen
- Tilret URIs, således at den URL der står der, peger på DW i det miljø du installerer i. URLer:  
  - DW PROD:  http://172.20.242.43:7333/StyretFiloverfoerselModtagAnmodService
  - DW TFE:   http://172.20.242.127:7333/StyretFiloverfoerselModtagAnmodService

#### FTP (Almindelig)
- I træstrukturen, gå til *All Projects -> Datawarehouseintegration -> Resources -> DatawarehouseDomainValues*
- Tilret værdierne ud fra det miljø der arbejdes på. 
*Første kolonne "Environment", skal ikke tilrettes, da de angiver de miljøer opsætningen er gældende for.*

#### SFTP (Private/Public key)
- I træstrukturen, gå til *All Projects -> Datawarehouseintegration -> Resources -> DatawarehouseSFTP*
*Første kolonne "Environment", skal ikke tilrettes, da de angiver de miljøer opsætningen er gældende for.*

### Integration: Captia/Workzone
- I træstrukturen, gå til *All Projects -> Datawarehouseintegration -> Resources -> DatawarehouseSFTP*
*Første kolonne "Environment", skal ikke tilrettes, da de angiver de miljøer opsætningen er gældende for.*
		
		
		
		
		
		
	
