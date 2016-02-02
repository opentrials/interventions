# Interventions

A Data Package which is a database of public and private sources of
information on interventions related to clinical trials.

In addition, this README tries to provide some guidance on how one
could take info from these multiple resources to create a new,
normalized list of drugs.

## NDC

One way to link at least some of these databases is through the
[NDC](http://www.drugs.com/ndc.html). The NDC, or National Drug Code,
is a unique 10-digit, 3-segment number. It is a universal product
identifier for human drugs in the United States. This is used by both
DrugBank and FDA.

**DrugBank XML**

```
<product>

    <name>Pulmozyme</name>
    <ndc-id>50242-100\_1f306717-b937-4efc-a269-bcadda447cce</ndc-id>
    <ndc-product-code>50242-100</ndc-product-code>
    ...
```

API request for [50242-100](https://api.fda.gov/drug/label.json?search=openfda.product_ndc:%2250242-100%22) on FDA.


## MeSH

Drugs (interventions) may also be linked to trials (in
ClinicialTrials.gov) via MeSH. The following XML snippet from
[NCT00420498](https://clinicaltrials.gov/ct2/show/NCT00420498?term=NCT00420498&rank=1)
associates this trial with a drug term found in MeSH.

**Clinical Trials XML**

```
<intervention_browse>
    <!-- CAUTION: The following MeSH terms are assigned with an imperfect 
         algorithm -->
    <mesh_term>Atomoxetine</mesh_term>
</intervention_browse>
```
