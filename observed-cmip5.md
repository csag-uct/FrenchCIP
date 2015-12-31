Observations historiques du climat:
----------------------

Le graphique ci‐dessous detaille different variables climatiques pour cette position.  Ces informations aident l’identification d’évènements climatiques specifiques tels que inondations et sécheresses, mais aussi d’observer la variabilité ou les tendances à long terme. 

De plus, il est souvent pertinent d’étudier la saisonnalité moyenne historique qui décrit les valeurs moyennes des variables climatiques à différentes periodes de l’année. 

CONSEIL : sélectionnez les différentes variables en utilisant le menu déroulante en haut du graphique.

<div class='plot-container700' id='plot1'></div>

<script>
	
	console.log('START');
	var plot1 = new monthlyTimeseries($('#plot1'), 24, 1396, {

		baseurl: "/climatedb/data/summary2/1/",
		title: "Observed monthly values",

		series: [{
			name: 'Précipitations totales mensuelles',
			units: 'mm',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_totals&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Nombre de jours de pluie mensuelles',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_days&statlow=0.2&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Nombre de jours de forte pluie mensuelles (> 5mm)',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_days&statlow=5&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Nombre de jours de forte pluie mensuelles (> 10mm)',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_days&statlow=10&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Nombre de jours de forte pluie mensuelles (> 20mm)',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_days&statlow=20&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Nombre de jours de forte pluie mensuelles (> 95e centile des jours de pluie observés)',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_days&statlow=95th&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Précipitations quotidienne moyenne',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_means&statlow=0.5&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Durée moyenne des sécheresses (jours)',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_spell_lengths&stathigh=0.2&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Précipitations quotidienne maximale',
			units: 'days',
			param: 'observed=observed&format=json&vars=ppt&statistic=monthly_maximums&statlow=0.5&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {
				type: 'column',
				color: '#8080ff',
				dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Température maximale moyenne',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Température maximale maximale',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Jours chauds mensuels (température maximale > 36C)',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_days&statlow=36&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'column',
				color: '#ff8080'
			}
		},{
			name: 'Durée de chaleur mensuel (jours > 95e centile)',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_spell_lengths&statlow=95th&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'column',
				color: '#ff8080',
                                dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Jours chauds mensuels (température maximale > 95e centile)',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_days&statlow=95th&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'column',
				color: '#ff8080',
                                dataGrouping: {
					approximation: 'average',
					groupPixelWidth: 15,
					units: [
						['month', [1,12]]
					]
				},
			}
		},{
			name: 'Température maximale minimale',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_minimums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Température minimale moyenne',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmin&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Température minimale maximale',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmin&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Température minimale minimale',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmin&statistic=monthly_minimums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		}],
		
		controls: {
			seriesSelector: 'options'
		}
	});
</script>
