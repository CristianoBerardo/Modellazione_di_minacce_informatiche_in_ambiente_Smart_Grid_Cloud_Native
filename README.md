# Sommario

La transizione globale verso un paradigma energetico sostenibile ha accelerato l’evoluzione delle reti
elettriche tradizionali in Smart Grid. Questa trasformazione, caratterizzata dall’integrazione di fonti
rinnovabili e dalla partecipazione attiva dei consumatori (_prosumer_), impone requisiti di scalabilità,
resilienza e capacità di elaborazione dati che le architetture IT convenzionali faticano a soddisfare. In
risposta, le infrastrutture critiche stanno adottando sempre più il paradigma _Cloud-Native_, che pro-
mette agilità, efficienza e robustezza attraverso tecnologie come la containerizzazione e l’orchestrazione
con Kubernetes.


Tuttavia, se da un lato l’adozione del cloud offre vantaggi significativi, dall’altro introduce nuove
e complesse superfici di attacco, esponendo le operazioni della rete energetica a minacce informatiche
sofisticate. La sicurezza di tali sistemi diventa, quindi, una priorità non negoziabile.


Il presente elaborato si pone l’obiettivo di analizzare e modellare sistematicamente le minacce
informatiche in un’architettura Smart Grid progettata secondo i principi Cloud-Native. Il lavoro si
articola in tre fasi principali:

1. **Analisi del Dominio**: Viene presentata un’analisi dettagliata dell’architettura della Smart
Grid, dai componenti di produzione fino al dominio del consumatore e operazionale, evidenziando
le tecnologie chiave come AMI, SCADA, EMS e DMS.
2. **Proposta Architetturale**: Viene definito un modello architetturale Cloud-Native per la Smart
Grid, basato su una federazione di cluster Kubernetes isolati (_Trusted Boundaries_) che gestiscono
i diversi domini funzionali (AMI, DMS, EMS), garantendo robustezza e autonomia operativa.
3. **Modellazione delle Minacce**: Viene applicata la metodologia formale del Threat Modeling.

Utilizzando un Diagramma di Flusso dei Dati (DFD) per rappresentare l’architettura, si applica
il framework STRIDE (_**S**poofing, **T**ampering, **R**epudiation, **I**nformation Disclosure, **D**enial of
Service, **E**levation of Privilege_) per identificare, classificare e analizzare sistematicamente le
potenziali minacce.


L’analisi ha permesso di individuare vulnerabilità critiche, come attacchi di _Tampering_ ai dati
provenienti dai PMU, _Denial of Service_ contro i sistemi SCADA ospitati nel cloud e attacchi di _Eleva-
tion of Privileg_ e per il controllo coordinato di dispositivi remoti. Per ciascuna minaccia significativa,
vengono proposte strategie di mitigazione e contromisure di sicurezza specifiche per il contesto _Cloud-Native_, 
tra cui l’uso di database WORM, la segmentazione dei privilegi tramite RBAC e l’adozione di
best practice per la sicurezza dei container e dei cluster.


Il contributo principale di questa tesi risiede nell’applicazione strutturata di una metodologia di
sicurezza proattiva (”_Secure by Design_”) a un’infrastruttura critica moderna, fornendo un modello
concreto per l’analisi dei rischi in sistemi ciber-fisici complessi e distribuiti.

# Il Dominio del Consumatore


<img width="1302" height="511" alt="image" src="https://github.com/user-attachments/assets/84546e93-3dda-4d21-8f46-da48332930f1"/>


# Il Dominio Operazionale


<img width="1032" height="465" alt="image" src="https://github.com/user-attachments/assets/d5f16186-0ab1-4fc6-83bb-9b6cbfc64e22" />


# L'Architettura Smart Grid Cloud-Native proposta


<img width="741" height="599" alt="image" src="https://github.com/user-attachments/assets/bb1ca25a-c793-430d-b651-e46e35349324" />


