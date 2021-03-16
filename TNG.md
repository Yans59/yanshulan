## Illustris TNG
The TNG simulation is from a starting redshift of  z = 127 to the present day , z = 0.
The TNG50 enables a mass resolution which is more than a hundred times better than in the TNG300 simulation , the TNG50-1 is the highest resolution realizations , including $$2\times2160^3$$ resolution elements.

## Data
(More details is in the [TNG data specifications webpage](https://www.tng-project.org/data/docs/specifications/))

### Snapshots
There are 100 snapshots stored for every run. The ' full ' snapshots encompass the entire volume , the ' mini ' snapshots only have a subset of particle fields available. 

Particles within the snapshot files are sorted according to their group / subgroup / memberships. 

Separate " subbox " cutouts exist for each baryonic run. These are spatial cutouts of fixed comoving size and fixed comoving coordinates , and the primary benefit is that their time resolutio is significantly better than that of the main snapshots. There are **two subboxes for TNG100** and **three subboxes for TNG50 and TNG300**.

- **Notes** : 
	- The time spacing of the subboxes is note uniform in scale factor or redshift , but scales withe the time integration hierarchy of the simulation , and is thus variable , with some discrete factor of two jumps at several points during the simulations.
	- The subboxes , unlike the full box , are not periodic.

### Group Catalogs
There is on group catalog associated with each snapshot , which includes both FoF and Subfind objects. Every HDF5 group catalog contains the following groups : Header , Group , Subhalo. 
- "Group" , "FoF Group", and "FoF Halo" all refer to halos.
- "Subgroup", "Subhalo", and "Subfind Group" all refer to subhalos.
- The first (most massive) subgroup of each halo is the "Primary Subgroup" or "Central Subgroup".
- All other following subgroups within the same halo are "Secondary Subgroups", or "Satellite Subgroups".

### Supplementary Data Catalogs
#### Molecular and atomic hydrogen (HI + HII ) galaxy contents
(More details and tables are in the webpage : https://www.tng-project.org/data/docs/specifications/#sec5i)

This catalog contains post-processed modeling of atomic (HI) and molecular (HII) hydrogen, on a per subhalo (i.e. per galaxy) basis. The total mass of each component is available, as well as pre-computed radial profiles. Note that all results sum, by construction, over the gas cells gravitationally bound to each subhalo only. 

**Simulations and snapshot coverage** : 
- Available for: TNG50-1, TNG100-1, TNG100-2, TNG300-1, and Illustris-1.
- For each, redshifts: z=0, z=0.5, z=1, z=1.5, and z=2 (five snapshots per run).

The galaxy selection was designed to be complete both in stellar and in gas mass, i.e., a galaxy needs to either exceed the minimum stellar OR the minimum gas mass. 