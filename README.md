def distribuir_nomina(monto):
    if monto < 500 or monto > 5000:
        return "El monto debe estar entre 500 y 5000."

    # Inicializar conteos de billetes
    billetes_500 = 0
    billetes_100 = 0
    billetes_50 = 0
    billetes_20 = 0
    billetes_10 = 0

    if monto > 2500:
        # Distribución para nómina > 2500
        billetes_500 = min(monto // 500, 4)
        monto -= billetes_500 * 500

        billetes_100 = min(monto // 100, 10)
        monto -= billetes_100 * 100

        billetes_50 = min(monto // 50, 5)
        monto -= billetes_50 * 50

        billetes_20 = min(monto // 20, 7)
        monto -= billetes_20 * 20

    else:
        # Distribución para nómina <= 2500
        billetes_500 = min(monto // 500, 2)
        monto -= billetes_500 * 500

        billetes_100 = min(monto // 100, 5)
        monto -= billetes_100 * 100

        billetes_50 = min(monto // 50, 5)
        monto -= billetes_50 * 50

        billetes_20 = min(monto // 20, 14)
        monto -= billetes_20 * 20

    # Billetes de 10 para lo que quede
    billetes_10 =
