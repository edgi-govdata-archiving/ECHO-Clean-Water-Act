# ECHO-CWA-Compliance
Use EPA's ECHO datasets to view compliance violations by quarter for state/congressional districts.

The analysis uses NPDES_QNCR_HISTORY for the CWA compliance data, and ECHO_EXPORTER for facilities
mapped into states and congressional districts.  The ECHO_EXPORTER data has been pre-filtered by
an SQL query to obtain just the facility information (not used), derived congressional district and
census block, for the records with NPDES_FLAG = 'Y':

select registry_id, fac_name, fac_city, fac_state, fac_zip, fac_county, 
fac_lat, fac_long, npdes_flag, npdes_ids, fac_derived_cd113, fac_derived_cb2010
from echo_exporter where npdes_flag = 'Y'

The results of this query are saved into ECHO_EXPORTER_NPDES.csv.
