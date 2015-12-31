Observation du climat passé:
----------------------

Le graphique ci‐dessous présente differentes variables du climat passé pour cette station. Ces informations aident à l’identification d’évènements climatiques spécifiques tels que innondations ou sécheresses, mais cela permet aussi d’observer la variabilité ou les tendances climatiques à long terme. 

De plus, il est souvent intéressant de pouvoir observer les variations moyennes saisonniaires, caractérisées par les valeurs moyennes de differentes variables climatiques à différentes periodes de l’année.

Les projections du futur climat, dont l'échelle est réduite statistiquement, sont aussi disponible pour cette station.

CONSEIL : sélectionnez les différentes variables en utilisant le menu déroulant en haut du graphique.

CONSEIL : 

<div class='plot-container700' id='plot1'></div>

<script>
	
	console.log('START');
	var plot1 = new monthlyTimeseries($('#plot1'), 24, 1396, {

		baseurl: "/climatedb/data/summary2/1/",
		title: "Observed monthly values",

		series: [{
			name: 'Précipitations totales par mois',
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
			name: 'Nombre de jours pluvieux par mois',
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
			name: 'Nombre de jours de forte pluie par mois (> 5mm)',
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
			name: 'Nombre de jours de forte pluie par mois (> 10mm)',
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
			name: 'Nombre de jours de forte pluie par mois (> 20mm)',
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
			name: 'Nombre de jours de forte pluie par mois (> 95ème percentile des jours pluvieux)',
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
			name: 'Moyennes des précipitations par jour',
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
			name: 'Durée moyenne de sécheresse (en jours)',
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
			name: 'Maximum des précipitations par jour',
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
			name: 'Moyenne des températures maximales',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Maximum des températures maximales',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Nombre de jours très chaud par mois (température maximale > 36 degC)',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_days&statlow=36&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'column',
				color: '#ff8080'
			}
		},{
			name: 'Durée de canicule par mois (en jours > 95ème percentile)',
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
			name: 'Nombre de jours très chaud par mois (température maximale > 95ème percentile)',
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
			name: 'Minimum des températures maximales',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmax&statistic=monthly_minimums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Moyenne des températures minimales',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmin&statistic=monthly_means&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Maximum des températures minimales',
			units: '\u00B0C',
			param: 'observed=observed&format=json&vars=tmin&statistic=monthly_maximums&folder_id={{folder_id}}&extent_id={{extent}}',

			observed: {			
				type: 'spline',
				color: '#ff8080'
			}
		},{
			name: 'Minimum des températures minimales',
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
