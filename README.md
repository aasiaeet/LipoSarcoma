# LipoSarcoma
De-Differentiated LipoSarcoma, Modeling and Biomarker Detection

 - **Goal:** We want to detect the recurrence of De-Differentiated [[Liposarcoma]] (DDLS) early post surgery. 
    - **Context:** 
        - **Location issue:** This type of cancer is hard to detect in general for several reasons
            - It is close to other organs (kidney, etc.) therefore  radiography has a hard time detecting it. It usually gets detected when the tumor has become big, even up to the size of a volleyball. 
            - After surgery, it is hard to use radiography to detect early relapse because we can not distinguish between scar tissues and regrown tumor. We test the patient again in four months which may be too late. 
            - Because of the location, the biopsy is also challenging. 
        - **Treatment issue:**
            - In general, the first surgery can be curative in 10% of the cases other times the tumor grows back. After that, we can just prolong the survival by timely surgical intervention. 
                - It is a hard place to access and perform surgery. 
                - The recurred tumor is usually multifocal, i.e., there are multiple of them growing around the same place. Note that these are not multiple different tumors, they re from a unique clone but grown in multiple places in the same organ.
        - **Biology of the tumor:** 
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Faasiaeet%2Fh4ljCDlyG4.png?alt=media&token=3313d068-d14e-4700-b0d0-454fdbcae0b8)
            - We know that there are [[Exosome]] carrying around stuff from the tumor to the micro-environment and nearby cells. Some cargos of these extracellular vesicles (EVs) in the DDLS case are miRNA-25/92 and MDM2. 
            - miRNA cargo of the EV, when unloaded in macrophages, causes the release of [[IL6]] which is associated with metastasis and tumor microenvironment.
            - MDM2 cargo of the EV when getting to pre-[[Adipocytes]] down-regulate p53 and promote proliferation. They also make the P-a releases [[MMP2]] which is a protein that breaks down the extracellular matrix and helps metastasis.
    - **Questions: ** There are five parameters in this problem: tumor size, the number of focals, and the fraction of de-differentiated cells in the tumor, MDM2 (or miRNAs) level in the blood, and survival. 
        - Can we detect the recurrence using MDM2/miRNAs level in blood? 
        - What is the relationship between MDM2 and the tumor size? Does it correlate with tumor volume or surface? 
            - Since the recurred tumor is multifocal, how should we model that spatially? Probably, in the 3D model, some of the cells should migrate and start a new tumor. 
            - Can we have two macro stages for tumor cells: de-differentiated and differentiated? What are the properties of these two?
        - Can we predict survival using the other four parameters? 
