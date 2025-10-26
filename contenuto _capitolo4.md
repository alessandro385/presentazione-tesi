<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pannello di Controllo Forecasting</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 40px;
            max-width: 1200px;
            width: 100%;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
        }

        .header h1 {
            color: #2d3748;
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .header p {
            color: #718096;
            font-size: 1.1em;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-bottom: 50px;
        }

        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .btn-primary {
            background: linear-gradient(135deg, #3182ce, #2c5282);
            color: white;
        }

        .btn-warning {
            background: linear-gradient(135deg, #f6ad55, #ed8936);
            color: white;
        }

        .btn-success {
            background: linear-gradient(135deg, #48bb78, #38a169);
            color: white;
        }

        .workflow {
            position: relative;
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .workflow-row {
            display: flex;
            justify-content: space-around;
            gap: 20px;
            flex-wrap: wrap;
        }

        .workflow-card {
            background: linear-gradient(135deg, #f7fafc, #edf2f7);
            border-radius: 15px;
            padding: 30px;
            flex: 1;
            min-width: 250px;
            max-width: 350px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            position: relative;
            border: 2px solid #e2e8f0;
            transition: all 0.3s ease;
        }

        .workflow-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
            border-color: #667eea;
        }

        .workflow-card h3 {
            color: #2d3748;
            font-size: 1.3em;
            margin-bottom: 10px;
            text-align: center;
        }

        .workflow-card p {
            color: #4a5568;
            line-height: 1.6;
            text-align: center;
            font-size: 0.95em;
        }

        .arrow {
            text-align: center;
            color: #667eea;
            font-size: 2em;
            margin: 10px 0;
        }

        .step-number {
            position: absolute;
            top: -15px;
            left: 20px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(102, 126, 234, 0.3);
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }

            .header h1 {
                font-size: 1.8em;
            }

            .workflow-card {
                max-width: 100%;
            }

            .button-group {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📊 Pannello di Controllo Forecasting</h1>
            <p>Sistema integrato per l'analisi e la previsione dei consumi</p>
        </div>

        <div class="button-group">
            <button class="btn btn-primary">Aggiorna Dati SQL</button>
            <button class="btn btn-primary">Addestra Modello L1</button>
            <button class="btn btn-primary">Addestra Modello L2</button>
            <button class="btn btn-primary">Esegui Forecast</button>
            <button class="btn btn-primary">Esegui Backtest</button>
            <button class="btn btn-success">Genera Ordini</button>
            <button class="btn btn-warning">Verifica Ordini</button>
        </div>

        <div class="workflow">
            <div class="workflow-row">
                <div class="workflow-card">
                    <div class="step-number">1</div>
                    <h3>🔄 Aggiornamento Dati SQL</h3>
                    <p>Acquisizione e aggiornamento dei dati consumi e meteo dal database SQL</p>
                </div>

                <div class="workflow-card">
                    <div class="step-number">2</div>
                    <h3>🎯 Addestramento Modello L1</h3>
                    <p>Training del modello di correzione meteo livello 1 con algoritmi avanzati</p>
                </div>

                <div class="workflow-card">
                    <div class="step-number">3</div>
                    <h3>🔧 Addestramento Modello L2</h3>
                    <p>Addestramento del modello correttivo del forecast base con parametri ottimizzati</p>
                </div>
            </div>

            <div class="arrow">↓</div>

            <div class="workflow-row">
                <div class="workflow-card">
                    <div class="step-number">4</div>
                    <h3>📈 Esecuzione Forecast</h3>
                    <p>Generazione delle previsioni finali attraverso elaborazione forecasting</p>
                </div>

                <div class="workflow-card">
                    <div class="step-number">5</div>
                    <h3>🧪 Esecuzione Backtest</h3>
                    <p>Validazione delle performance del modello tramite analisi storica</p>
                </div>
            </div>

            <div class="arrow">↓</div>

            <div class="workflow-row">
                <div class="workflow-card">
                    <div class="step-number">6</div>
                    <h3>✅ Generazione Ordini</h3>
                    <p>Creazione automatica degli ordini sulla base delle previsioni elaborate</p>
                </div>

                <div class="workflow-card">
                    <div class="step-number">7</div>
                    <h3>🔍 Verifica Ordini</h3>
                    <p>Controllo e validazione finale degli ordini generati dal sistema</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>