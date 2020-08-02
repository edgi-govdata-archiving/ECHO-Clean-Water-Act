 [![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](https://github.com/edgi-govdata-archiving/overview/blob/master/CONDUCT.md)

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

Repo websites

[echo-cwa-compliance-violations](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliance-violations.ipynb)

[CWA_Inspections](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliances-inspections.ipynb)

[CWA_Enforcements.ipynb](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-enforcements.ipynb)

---

## Notebook validation

### Link to Notebooks

[echo-cwa-compliance-violations](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliance-violations.ipynb)

[CWA_Inspections](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-compliances-inspections.ipynb)

[CWA_Enforcements.ipynb](https://colab.research.google.com/github/edgi-govdata-archiving/ECHO-Clean-Water-Act/blob/master/echo-cwa-enforcements.ipynb)

## License & Copyright

Copyright (C) <year> Environmental Data and Governance Initiative (EDGI)
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3.0.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

See the [`LICENSE`](/LICENSE) file for details.
