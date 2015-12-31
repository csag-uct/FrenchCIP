Projections climatiques du futur (CMIP5 réduite)
------------------------------------------------
Le graphique ci-dessous montre la gamme des changements futurs projetés pour ce lieu sur 10 CMIP5 modèles climatiques généraux (MCG) de réduction d’échelle statistique pour 2 <a href='#nodes/rcp'>scénarios RCP</a> différents (RCP 4.5 et RCP 8.5).  <strong>Les anomalies sont calculées par rapport à la période historique 1980-2000</strong>.  Les barres pleines représentent la gamme entre les 80% intermédiaires du change projeté et donc les 10% supérieur et inférieurs sont exclus à cause d’être souvent considérés des valeurs aberrante.  Cependant, les lignes grises montrent les changements projetés pour chaque modèle, donc il est possible de voir comment chaque modèle (intentionnellement pas nommé) projeter les changements futurs. 

<div class='content-section'>
<div class='content-section-header'>Monthly anomaly calculations</div>
<div class='content-section-detail'>
<p>
Les anomalies mensuelles pour un modèle particulier sont calculées comme la différence entre la moyenne à long terme (20 ans) pour un certain mois au période futur, moins la moyenne à long terme pour un certain mois au période historique.  En conséquence, les anomalies représentent des changements dans la climatologie à long terme pour un mois donné.  Ils ne représentent pas d’informations sur la  variabilité plus courte terme ou des extrêmes. </p>
<p>
Quand les anomalies de la variété des modèles ont été calculées pour un mois particulier, c’est donc possible de calculer statistiquement le 10e au 90e centiles de la distribution résultante.  Ceci aide simplement visualiser et simplifier l’information présentée en enlevant les anomalies extrêmes et en cachent les détails des anomalies de modèles individuels. 
</div>
</div>

Cliquez sur « observé » dans la légende pour afficher les magnitudes observées.  Pour plus de détails, <a href='#nodes/seasonality-cmip5'>explorez le climat observé</a> pour cet endroit.  Utilisez les options du graphique pour sélectionner les combinaisons différentes de variables/scénarios et utilisez le curseur pour choisir la période future.  

<div class='plot-container700' id='plot1'></div>

<script>
	
	console.log('START');
	var plot1 = new monthlyAnomalies($('#plot1'), 24, 1396, {
                baseurl: "/climatedb/data/summary2/1/",
		title: "Decadal running means",
		series: [{
			name: 'Précipitations totales mensuelles RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_totals&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'mm',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Précipitations totales mensuelles RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_totals&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'mm',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_days&statlow=0.2&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_days&statlow=0.2&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie > 5mm RCP 8.5',
			units: 'days',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_days&statlow=5&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie > 5mm RCP 4.5',
			units: 'days',
			param: 'observed=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_days&statlow=5&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie > 20mm RCP 8.5',
			units: 'days',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_days&statlow=20&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie > 20mm RCP 4.5',
			units: 'days',
			param: 'observed=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_days&statlow=20&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie > 95e centile des jours de pluie observés RCP 8.5',
			units: 'days',
			param: 'observed=observed&pseries=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_days&statlow=95th&dailystatlow=0.0&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Nombre de jours de pluie >  95e centile des jours de pluie observés RCP 4.5',
			units: 'days',
			param: 'observed=observed&pseries=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_days&statlow=95th&dailystatlow=0.0&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Précipitations quotidienne maximale RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'mm',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Précipitations quotidienne maximale RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'mm',
			observed: {},
			future: {
                            increase_color: '#4572A7',
                            decrease_color: ' #AA4643'
                        }
		},{
			name: 'Durée moyenne des sécheresses RCP 8.5',
			units: 'days',
			param: 'observed=observed&future=RCP8.5&format=json&vars=ppt&statistic=monthly_spell_lengths&stathigh=0.2&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {}
		},{
			name: 'Durée moyenne des sécheresses RCP 4.5',
			units: 'days',
			param: 'observed=observed&future=RCP4.5&format=json&vars=ppt&statistic=monthly_spell_lengths&stathigh=0.2&folder_id={{folder_id}}&extent_id={{extent}}',
			observed: {},
			future: {}
		},{
			name: 'Température maximale moyenne RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=tmax&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',
			units: '\u00B0C',
			observed: {},
			future: {}
		},{
			name: 'Température maximale moyenne RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=tmax&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',
			units: '\u00B0C',
			observed: {},
			future: {}
		},{
			name: 'Température minimale moyenne RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=tmin&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',
			units: '\u00B0C',
			observed: {},
			future: {}
		},{
			name: 'Température minimale moyenne RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=tmin&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',
			units: '\u00B0C',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 32\u00B0) RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=tmax&statistic=monthly_days&statlow=32&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 32\u00B0) RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=tmax&statistic=monthly_days&statlow=32&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 36\u00B0) RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=tmax&statistic=monthly_days&statlow=36&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 36\u00B0) RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=tmax&statistic=monthly_days&statlow=36&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 95e centile des jours observés) RCP 8.5',
			param: 'observed=observed&pseries=observed&future=RCP8.5&format=json&vars=tmax&statistic=monthly_days&statlow=95th&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours chauds (tmax > 95e centile des jours observés) RCP 4.5',
			param: 'observed=observed&pseries=observed&future=RCP4.5&format=json&vars=tmax&statistic=monthly_days&statlow=95th&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Heat spell duration 95th percentile threshold RCP 8.5',
			param: 'observed=observed&pseries=observed&future=RCP8.5&format=json&vars=tmax&statistic=monthly_spell_lengths&statlow=95th&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Durée de chaleur, seuil de 95e centile RCP 4.5',
			param: 'observed=observed&pseries=observed&future=RCP4.5&format=json&vars=tmax&statistic=monthly_spell_lengths&statlow=95th&dailystathigh=999&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours de gel (tmin < 0\u00B0) RCP 8.5',
			param: 'observed=observed&future=RCP8.5&format=json&vars=tmin&statistic=monthly_days&stathigh=0&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		},{
			name: 'Jours de gel (tmin < 0\u00B0) RCP 4.5',
			param: 'observed=observed&future=RCP4.5&format=json&vars=tmin&statistic=monthly_days&stathigh=0&folder_id={{folder_id}}&extent_id={{extent}}',
			units: 'days',
			observed: {},
			future: {}
		}],
		controls: {
			seriesSelector: 'options'
		}
	});
</script>
