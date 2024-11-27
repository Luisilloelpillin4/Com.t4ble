<!doctype html>
<html lang="en">

<head>
    <title>Calc</title>
    <!-- Required meta tags -->

    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">


    <!-- <link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css" rel="stylesheet" /> -->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;500&display=swap" rel="stylesheet">
    <script
        src="https://cdn.jsdelivr.net/combine/npm/vue@2.6.14/dist/vue.min.js,npm/accounting-js@1.1.1,npm/vue@2.5.16,npm/vue-numeric@2.3.0,npm/@vue/composition-api@1.4.3,npm/echarts@5.2.2,npm/vue-echarts@6.0.2,npm/papaparse@5.4.1/papaparse.min.js"></script>
    <script src="https://smtpjs.com/v3/smtp.js"></script>
    <style type="text/css">
        body {
            background-image: linear-gradient(-225deg, #E3FDF5 0%, #FFE6FA 100%);
        }

        .form-control form-control-sm {
            /* border-radius: 0; */
            width: 140px;
            margin: 0 auto;
        }

        .btn-group {
            width: 140px;
        }

        .list-group-item {
            padding-top: 1.75rem;
        }

        .vue-slider-mark-label {
            font-size: 10px;
            color: #007bff;
        }

        .vue-slider-process {
            /* background-color: #004a9b; */
            background-color: rgb(228, 107, 12);
            border-radius: 15px;
        }

        .vue-slider-dot-handle {
            cursor: pointer;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            box-sizing: border-box;
        }

        .tableBorder {
            border: 1.8px solid #004a9b;
        }

        th,
        td {
            padding-left: 30px !important;
        }
    </style>

</head>

<body class="bg-light demo">

    <div class="container-fluid my-5" id="app">

        <div class="row justify-content-center">

            <div class="col-md-12">
                <h3 class="text-center">ESTRUCTURA DE COSTOS </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">
                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table1">

                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th class="text-left">COSTOS FIJOS</th>
                                    <th>Semana 1</th>
                                    <th>Semana 2</th>
                                    <th>Semana 3</th>
                                    <th>Semana 4</th>
                                    <th>Mensual</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td class="text-left">Renta del local</td>
                                    <td> <vue-numeric v-model="C9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric v-model="D9" separator="," thousand-separator="." :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G9" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">Energía eléctrica</td>
                                    <td> <vue-numeric v-model="C10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="D10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G10" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">Internet</td>
                                    <td> <vue-numeric v-model="C11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="D11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G11" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">Agua potable</td>
                                    <td> <vue-numeric v-model="C12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="D12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G12" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">Transporte</td>
                                    <td> <vue-numeric v-model="C13" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="D13" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E13" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F13" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G13" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">Sueldo de empleados</td>
                                    <td> <vue-numeric v-model="C14" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="D14" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="E14" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="F14" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric v-model="G14" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <th class="text-left"><strong>TOTAL</strong></th>
                                    <th><strong> <vue-numeric v-model="C17" read-only :precision="2"
                                                class="form-control  form-control-sm " currency="$"
                                                currency-symbol-position="preffix"
                                                style="width: 100%;"></vue-numeric></strong></th>
                                    <th><strong> <vue-numeric v-model="D17" read-only :precision="2"
                                                class="form-control  form-control-sm " currency="$"
                                                currency-symbol-position="preffix"
                                                style="width: 100%;"></vue-numeric></strong></th>
                                    <th><strong> <vue-numeric v-model="E17" read-only :precision="2"
                                                class="form-control  form-control-sm " currency="$"
                                                currency-symbol-position="preffix"
                                                style="width: 100%;"></vue-numeric></strong></th>
                                    <th><strong> <vue-numeric v-model="F17" read-only :precision="2"
                                                class="form-control  form-control-sm " currency="$"
                                                currency-symbol-position="preffix"
                                                style="width: 100%;"></vue-numeric></strong></th>
                                    <th><strong> <vue-numeric v-model="G17" read-only read-only :precision="2"
                                                class="form-control  form-control-sm " currency="$"
                                                currency-symbol-position="preffix"
                                                style="width: 100%;"></vue-numeric></strong></th>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
                <h3 class="text-center mt-3">Trabajador
                </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">
                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table2">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th class="text-left">Trabajador </th>
                                    <th>Semana 1 </th>
                                    <th>Semana 2 </th>
                                    <th>Semana 3 </th>
                                    <th>Semana 4</th>
                                    <th>Mensual </th>
                                </tr>
                            </thead>
                            <tbody>

                                <tr>
                                    <td class="text-left">A</td>
                                    <td> <vue-numeric v-model="J8" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric v-model="K8" separator="," thousand-separator="." :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="L8" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="M8" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric :value="N8" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">B</td>
                                    <td> <vue-numeric v-model="J9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="K9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="L9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="M9" :precision="2" class="form-control  form-control-sm "
                                            currency="$" currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric :value="N9" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">C</td>
                                    <td> <vue-numeric v-model="J10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="K10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="L10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="M10" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric :value="N10" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left">D</td>
                                    <td> <vue-numeric v-model="J11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="K11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="L11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td> <vue-numeric v-model="M11" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <th> <vue-numeric :value="N11" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                                <tr>
                                    <td class="text-left"></td>
                                    <th> <vue-numeric read-only v-model="J12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                    <th> <vue-numeric read-only v-model="K12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                    <th> <vue-numeric read-only v-model="L12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                    <th> <vue-numeric read-only v-model="M12" :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                    <th> <vue-numeric :value="N12" read-only :precision="2"
                                            class="form-control  form-control-sm " currency="$"
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                            </tbody>

                        </table>
                    </div>
                </div>
                <h3 class="text-center mt-3">COSTOS VARIABLES
                </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">
                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table3">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th>PRODUCTO</th>
                                    <th>PRESENTACION</th>
                                    <th>CANTIDAD</th>
                                    <th>UNIDAD</th>
                                    <th>PRECIO</th>
                                    <th>COSTO UNITARIO</th>
                                </tr>
                            </thead>
                            <tbody>

                                <tr>
                                    <td>Atomizador</td>
                                    <td>Paquete 300 ml</td>
                                    <td>
                                        <vue-numeric v-model="CC5" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>Ind</td>
                                    <td>
                                        <vue-numeric v-model="CE5" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF5"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Albahaca</td>
                                    <td>Kilo</td>
                                    <td>
                                        <vue-numeric v-model="CC6" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>gr</td>
                                    <td>
                                        <vue-numeric v-model="CE6" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF6"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Alcohol</td>
                                    <td>litro</td>
                                    <td>
                                        <vue-numeric v-model="CC7" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>ml</td>
                                    <td>
                                        <vue-numeric v-model="CE7" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF7"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Aceite de eucalipto</td>
                                    <td>pza</td>
                                    <td>
                                        <vue-numeric v-model="CC8" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>ml</td>
                                    <td>
                                        <vue-numeric v-model="CE8" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF8"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Agua</td>
                                    <td>litro</td>
                                    <td>
                                        <vue-numeric v-model="CC9" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>ml</td>
                                    <td>
                                        <vue-numeric v-model="CE9" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF9"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Etiquetas</td>

                                    <td>Paquete</td>
                                    <td>
                                        <vue-numeric v-model="CC10" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>ind</td>
                                    <td>
                                        <vue-numeric v-model="CE10" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF10"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>Bolsa de empaque</td>
                                    <td>Paquete</td>
                                    <td>
                                        <vue-numeric v-model="CC11" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>ind</td>
                                    <td>
                                        <vue-numeric v-model="CE11" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="CF11"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td><strong>TOTAL</strong></td>
                                    <td></td>
                                    <td></td>
                                    <td></td>
                                    <td></td>
                                    <th>
                                        <vue-numeric :precision="2" read-only :value="CF12"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </th>
                                </tr>
                            </tbody>

                        </table>
                    </div>
                </div>
                <h3 class="text-center mt-3">FICHA TECNIC
                </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">

                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table4">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th>CANTIDAD </th>
                                    <th> <vue-numeric v-model="DC6" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix"></vue-numeric></th>
                                    <th>COSTO UNITARIO </th>
                                    <th> <vue-numeric v-model="DE6" read-only class="form-control  form-control-sm "
                                            currency-symbol-position="preffix"></vue-numeric></th>
                                </tr>
                            </thead>

                        </table>
                    </div>

                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table5">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th>PRODUCTO</th>
                                    <th>CANTIDAD</th>
                                    <th>UNIDAD</th>
                                    <th>COSTO</th>
                                </tr>
                            </thead>
                            <tbody>

                                <tr>
                                    <td>
                                        <select v-model="DB8" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC8" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>Ind</td>
                                    <td>
                                        <vue-numeric :precision="2" read-only :value="DE8"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB9" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC9" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>gr</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE9"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB10" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC10" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>ml</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE10"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB11" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC11" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>ml</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE11"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB12" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC12" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>ml</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE12"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB13" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC13" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>ind</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE13"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td>
                                        <select v-model="DB14" class="form-control form-control-sm" name="" id="">
                                            <option value="Atomizador">Atomizador</option>
                                            <option value="Albahaca">Albahaca</option>
                                            <option value="Alcohol">Alcohol</option>
                                            <option value="Aceite de eucalipto ">Aceite de eucalipto </option>
                                            <option value="Agua">Agua</option>
                                            <option value="Etiquetas">Etiquetas</option>
                                            <option value="Bolsa de empaque">Bolsa de empaque</option>
                                        </select>
                                    </td>
                                    <td> <vue-numeric v-model="DC14" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>ind</td>
                                    <td><vue-numeric :precision="2" read-only :value="DE14"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                <tr>
                                    <td><strong>TOTAL</strong></td>
                                    <td></td>
                                    <td></td>
                                    <th><vue-numeric :precision="2" read-only :value="DE15"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></th>
                                </tr>
                            </tbody>

                        </table>
                    </div>
                </div>
                <h3 class="text-center mt-3">EMPRESA COMERCIAL (Compra productos y los revende)

                </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">

                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table6">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th colspan="3">PRODUCTO</th>
                                    <th>CANTIDAD</th>
                                    <th></th>
                                    <th></th>
                                </tr>
                            </thead>

                            <tbody>

                                <tr>
                                    <td colspan="3">Margen de utilidad</td>
                                    <td><vue-numeric currency="%" currency-symbol-position="suffix" v-model="EE20"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>

                                </tr>
                                <tr>
                                    <td colspan="3">IVA</td>
                                    <td><vue-numeric currency="%" currency-symbol-position="suffix" v-model="EE23"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>

                                <tr>
                                    <td colspan="1" style="width:100px;">PV</td>
                                    <td colspan="1" style="width:100px;"><vue-numeric :precision="2" read-only
                                            currency-symbol-position="suffix" :value="EE8"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                    <td colspan="1" style="width:100px;">IVA</td>
                                    <td colspan="1" id="IVA_Val1" style="width:100px;"><vue-numeric :precision="2"
                                            read-only currency-symbol-position="suffix" :value="EI8"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                    <td colspan="1" style="width:100px;">PV+IVA</td>
                                    <td colspan="1" id="PV_IV_Val" style="width:100px;"><vue-numeric :precision="2"
                                            read-only currency-symbol-position="suffix" :value="EL8"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>

                                <tr>
                                    <th colspan="6">EMPRESA PRODUCTORA (Elabora sus productos)</th>

                                <tr>
                                    <td colspan="1" style="width:100px;">PV</td>
                                    <td colspan="1" style="width:100px;"><vue-numeric :precision="2" read-only
                                            currency-symbol-position="suffix" :value="EE15"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                    <td colspan="1" style="width:100px;">IVA</td>
                                    <td colspan="1" style="width:100px;"><vue-numeric :precision="2" read-only
                                            currency-symbol-position="suffix" :value="EL15"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                    <td colspan="1" style="width:100px;">PV+IVA</td>
                                    <td colspan="1" style="width:100px;"><vue-numeric :precision="2" read-only
                                            currency-symbol-position="suffix" :value="EI15"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric></td>
                                </tr>
                                </tr>
                            </tbody>
                        </table>
                    </div>


                </div>
                <h3 class="text-center mt-3">PUNTO EQUILIBRIO

                </h3>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">

                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table7">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th>PRODUCTO</th>
                                    <th>CANTIDAD</th>

                                </tr>
                            </thead>

                            <tbody>
                                <tr>
                                    <td>COSTOS FIJOS</td>
                                    <td>
                                        <vue-numeric currency="$" read-only currency-symbol-position="suffix"
                                            :value="FB3" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>COSTOS VARIABLES </td>
                                    <td>
                                        <vue-numeric currency="$" read-only currency-symbol-position="suffix"
                                            :value="FB4" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>PRECIO DE VENTA </td>
                                    <td>
                                        <vue-numeric currency="$" read-only currency-symbol-position="suffix"
                                            :value="FB5" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>P.E</td>
                                    <td>
                                        <vue-numeric currency="$" read-only currency-symbol-position="suffix"
                                            :value="FB6" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>
                                <tr>
                                    <td>UTILIDADES</td>
                                    <td>
                                        <vue-numeric currency="$" read-only currency-symbol-position="suffix"
                                            :value="FB7" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric>
                                    </td>
                                </tr>

                            </tbody>
                        </table>
                    </div>


                </div>
                <div class="card shadow-lg" style="border-radius: 10px; border-top: 1px solid #a5a3a3;">

                    <div class="table-responsive">

                        <table class="table table-sm table-borderless p-2 " id="table8">
                            <thead>

                                <tr style="background-color: rgb(233, 231, 231);">
                                    <th>CANTIDAD</th>
                                    <th>VENTAS</th>
                                    <th>COSTOS</th>
                                    <th>UTILIDAD</th>
                                    <th></th>
                                </tr>
                            </thead>

                            <tbody>
                                <tr v-for="(x ,i) in PUNTOArray">
                                    <td> <vue-numeric v-model="x.CANTIDAD" class="form-control  form-control-sm "
                                            currency-symbol-position="preffix" style="width: 100%;"></vue-numeric></td>
                                    <td>

                                        <vue-numeric read-only :precision="2" currency="$" :value="x.CANTIDAD * FB5"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>

                                        <vue-numeric read-only :precision="2" currency="$" :value="FB3+FB4*x.CANTIDAD"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>
                                    <td>

                                        <vue-numeric read-only :precision="2" currency="$"
                                            :value="(x.CANTIDAD * FB5)-(FB3+FB4*x.CANTIDAD)"
                                            class="form-control  form-control-sm " currency-symbol-position="preffix"
                                            style="width: 100%;"></vue-numeric>
                                    </td>

                                    <td>
                                        <!-- <button v-if="i==Business.length-1" @click="addBusiness"
                                            class="btn btn-action btn-outline-success"> &#43; </button> -->
                                        <button @click="RemoveItem(i)" class="btn btn-action btn-outline-danger">
                                            -
                                        </button>
                                        <button v-if="i==PUNTOArray.length-1" @click="addBusiness"
                                            class="btn btn-action btn-outline-primary"> &#43; </button>
                                    </td>
                                </tr>
                                <tr>
                                    <td colspan="5" class="text-center">
                                        <button v-if="PUNTOArray.length==0" @click="addBusiness"
                                            class="btn btn-action btn-outline-primary"> Añadir fila
                                        </button>
                                    </td>

                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <v-chart autoresize style="width:100%;height:400px;" class="mb-5" :option="chart3" />

                </div>


                <div class="row mb-3 mt-3">
                    <div class="col-md-12 text-center">
                        <div class="btn-group">
                            <button class=" btn btn-primary mx-1 " @click="DownloadPDF"><i class="fa fa-arrow-down p-0"
                                    style="font-size: 17px;"></i>
                                Download PDF</button>

                        </div>
                    </div>
                </div>
            </div>
        </div>



    </div>


    <script>



        function number(n) {
            return (isNaN(parseFloat(n)) || !isFinite(n)) ? 0 : parseFloat(n);
        }


        function getOptimalDimentions(width, height) {
            var wMax = 160;
            var hMax = 120;

            //first try wmx

            w = wMax;
            h = height / (width / w);

            if (h <= hMax) return [w, h];

            //now fix the height
            h = hMax;
            w = width / (height / h);
            return [w, h];
        }

        function FV(rate, nper, pmt, pv, type) {
            var pow = Math.pow(1 + rate, nper),
                fv;

            pv = pv || 0;
            type = type || 0;

            if (rate) {
                fv = (pmt * (1 + rate * type) * (1 - pow) / rate) - pv * pow;
            } else {
                fv = -1 * (pv + pmt * nper);
            }
            return fv;
        }

        function FVFunction(rate, nper, pmt, pv, type) {
            var pow = Math.pow(1 + rate, nper),
                fv;

            pv = pv || 0;
            type = type || 0;

            if (rate) {
                fv = (pmt * (1 + rate * type) * (1 - pow) / rate) - pv * pow;
            } else {
                fv = -1 * (pv + pmt * nper);
            }
            return fv;
        }
      
     
        Vue.use(VueNumeric.default);
        Vue.component("v-chart", VueECharts);

        new Vue({
            el: '#app',

            data: {
                C9: 900,
                C10: 150,
                C11: 389,
                C12: 157,
                C13: 150,
                C14: 1000,
                C15: 0,
                C16: 0,

                D9: 0,
                D10: 0,
                D11: 0,
                D12: 0,
                D13: 150,
                D14: 1000,
                D15: 0,
                D16: 0,

                E9: 0,
                E10: 0,
                E11: 0,
                E12: 0,
                E13: 150,
                E14: 1000,
                E15: 0,
                E16: 0,

                F9: 0,
                F10: 0,
                F11: 0,
                F12: 0,
                F13: 150,
                F14: 1000,
                F15: 0,
                F16: 0,



                J8: 250, K8: 250, L8: 250, M8: 250,
                J9: 250, K9: 250, L9: 250, M9: 250,
                J10: 250, K10: 250, L10: 250, M10: 250,
                J11: 250, K11: 250, L11: 250, M11: 250,

                CC5: 4,
                CC6: 1000,
                CC7: 1000,
                CC8: 60,
                CC9: 1000,
                CC10: 4,
                CC11: 90,

                CE5: 52,
                CE6: 40,
                CE7: 75,
                CE8: 30,
                CE9: 12,
                CE10: 10,
                CE11: 90,



                DC8: 1,
                DC9: 75,
                DC10: 125,
                DC11: 5,
                DC12: 125,
                DC13: 1,
                DC14: 1,

                DB8: 'Atomizador',
                DB9: 'Albahaca',
                DB10: 'Alcohol',
                DB11: 'Aceite de eucalipto ',
                DB12: 'Agua',
                DB13: 'Bolsa de empaque',
                DB14: 'Etiquetas',

                EE20: 50,
                EE23: 16,

                DC6: 1,
                PUNTOArray: [
                    { CANTIDAD: 1 }
                    , { CANTIDAD: 2 }
                    , { CANTIDAD: 3 }
                    , { CANTIDAD: 4 }
                    , { CANTIDAD: 5 }
                    , { CANTIDAD: 6 }
                    , { CANTIDAD: 7 }
                    , { CANTIDAD: 8 }
                    , { CANTIDAD: 9 }
                    , { CANTIDAD: 10 }
                    , { CANTIDAD: 11 }
                    , { CANTIDAD: 12 }
                    , { CANTIDAD: 13 }
                    , { CANTIDAD: 14 }
                    , { CANTIDAD: 15 }
                    , { CANTIDAD: 16 }
                    , { CANTIDAD: 17 }
                    , { CANTIDAD: 18 }
                    , { CANTIDAD: 19 }
                    , { CANTIDAD: 20 }
                    , { CANTIDAD: 21 }
                    , { CANTIDAD: 22 }
                    , { CANTIDAD: 23 }
                    , { CANTIDAD: 24 }
                    , { CANTIDAD: 25 }
                    , { CANTIDAD: 26 }
                    , { CANTIDAD: 27 }
                    , { CANTIDAD: 28 }
                    , { CANTIDAD: 29 }
                    , { CANTIDAD: 30 }
                    , { CANTIDAD: 31 }
                    , { CANTIDAD: 32 }
                    , { CANTIDAD: 33 }
                    , { CANTIDAD: 34 }
                    , { CANTIDAD: 35 }
                    , { CANTIDAD: 36 }
                    , { CANTIDAD: 37 }
                    , { CANTIDAD: 38 }
                    , { CANTIDAD: 39 }
                    , { CANTIDAD: 40 }
                    , { CANTIDAD: 41 }
                    , { CANTIDAD: 42 }
                    , { CANTIDAD: 43 }
                    , { CANTIDAD: 44 }
                    , { CANTIDAD: 45 }
                    , { CANTIDAD: 46 }
                    , { CANTIDAD: 47 }
                    , { CANTIDAD: 48 }
                    , { CANTIDAD: 49 }
                    , { CANTIDAD: 50 }
                ]
            },
            computed: {
                chart3: function () {
                    var self = this;
                    debugger;
                    var onearray=[]
                    var twoarray=[]
                    var threearray=[]
                    var fourarray=[]
                    for (let index = 1; index < this.PUNTOArray.length; index++) {
                        onearray.push(index);
                        twoarray.push(this.PUNTOArray[index].CANTIDAD*this.FB5)
                        threearray.push(this.FB3+this.FB4*this.PUNTOArray[index].CANTIDAD)
                        fourarray.push((this.PUNTOArray[index].CANTIDAD * this.FB5)-(this.FB3+this.FB4*this.PUNTOArray[index].CANTIDAD))
                    }



                    options = {
                        legend: {
                            data: ['CANTIDAD', 'VENTAS','COSTOS','UTILIDAD'],
                            top: 'top',  // Position legend at the top

                        },
                        toolbox: {
                            feature: {
                                saveAsImage: {}
                            }
                        },
                        xAxis: {
                            type: 'category',
                            boundaryGap: false,


                        },
                        yAxis: {
                            type: 'value'
                        },
                        series: [
                            {
                                name: 'CANTIDAD',
                                type: 'line',
                                data: onearray,
                            },
                            {
                                name: 'VENTAS',
                                type: 'line',
                                data: twoarray
                            },{
                                name: 'COSTOS',
                                type: 'line',
                                data: threearray
                            },
                            {
                                name: 'UTILIDAD',
                                type: 'line',
                                data: fourarray
                            },
                        ],
                        toolbox: {
                            feature: {
                                saveAsImage: {
                                    title: 'Chart'
                                },
                                magicType: {
                                    type: ['line','bar']
                                },
                                restore: {}
                            }
                        },
                        legend: {
                            show: true,
                            labels: {
                                fontSize: 6,
                            },
                            pointStyle: 'circle',
                            pointRadius: 2,
                            type: 'scroll',
                            bottom: -6,
                        },
                        tooltip: {
                            trigger: 'axis',
                            axisPointer: {
                                type: 'cross'
                            }
                        },
                        dataZoom: [{
                            type: 'slider',
                            start: 0,
                            end: 100,
                            bottom: '5.5%',
                        }]
                    };

                    return options;
                },
                formattedValue() {
                    return this.formatCurrency(this.C9);
                },
                G9() {
                    return this.C9 + this.D9 + this.E9 + this.F9;
                },
                G10() {
                    return this.C10 + this.D10 + this.E10 + this.F10;
                },
                G11() {
                    return this.C11 + this.D11 + this.E11 + this.F11;
                },
                G12() {
                    return this.C12 + this.D12 + this.E12 + this.F12;
                },
                G13() {
                    return this.C13 + this.D13 + this.E13 + this.F13;
                },
                G14() {
                    return this.C14 + this.D14 + this.E14 + this.F14;
                },
                G15() {
                    return this.C15 + this.D15 + this.E15 + this.F15;
                },
                G16() {
                    return this.C16 + this.D16 + this.E16 + this.F16;
                },
                C17() {
                    return this.C9 + this.C10 + this.C11 + this.C12 + this.C13 + this.C14 + this.C15 + this.C16;
                },
                D17() {
                    return this.D9 + this.D10 + this.D11 + this.D12 + this.D13 + this.D14 + this.D15 + this.D16;
                },
                E17() {
                    return this.E9 + this.E10 + this.E11 + this.E12 + this.E13 + this.E14 + this.E15 + this.E16;
                },
                F17() {
                    return this.F9 + this.F10 + this.F11 + this.F12 + this.F13 + this.F14 + this.F15 + this.F16;
                },
                G17() {
                    return this.G9 + this.G10 + this.G11 + this.G12 + this.G13 + this.G14 + this.G15 + this.G16;
                }
                ,



                J12() {
                    return this.J8 + this.J9 + this.J10 + this.J11;
                },
                K12() {
                    return this.K8 + this.K9 + this.K10 + this.K11;
                },
                L12() {
                    return this.L8 + this.L9 + this.L10 + this.L11;
                },
                M12() {
                    return this.M8 + this.M9 + this.M10 + this.M11;
                },
                N12() {
                    return this.N8 + this.N9 + this.N10 + this.N11;
                },
                N8() {
                    return this.J8 + this.K8 + this.L8 + this.M8;
                },
                N9() {
                    return this.J9 + this.K9 + this.L9 + this.M9;
                },
                N10() {
                    return this.J10 + this.K10 + this.L10 + this.M10;
                },
                N11() {
                    return this.J11 + this.K11 + this.L11 + this.M11;
                },

                CF5: function () {
                    if (this.CC5 == 0) return 0;

                    return this.CE5 / this.CC5;
                },
                CF6: function () {
                    if (this.CC6 == 0) return 0;

                    return this.CE6 / this.CC6;
                },
                CF7: function () {
                    if (this.CC7 == 0) return 0;

                    return this.CE7 / this.CC7;
                },
                CF8: function () {
                    if (this.CC8 == 0) return 0;

                    return this.CE8 / this.CC8;
                },
                CF9: function () {
                    if (this.CC9 == 0) return 0;

                    return this.CE9 / this.CC9;
                },
                CF10: function () {
                    if (this.CC10 == 0) return 0;

                    return this.CE10 / this.CC10;
                },
                CF11: function () {
                    if (this.CC11 == 0) return 0;

                    return this.CE11 / this.CC11;
                },
                CF12: function () {


                    return (
                        this.CF5
                        + this.CF6
                        + this.CF7
                        + this.CF8
                        + this.CF9
                        + this.CF10
                        + this.CF11

                    )
                },

                DE8: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB8).Value
                    var y = x * this.DC8
                    return y;

                },
                DE9: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB9).Value
                    var y = x * this.DC9
                    return y;

                },
                DE10: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB10).Value
                    var y = x * this.DC10
                    return y;

                },
                DE11: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB11).Value
                    var y = x * this.DC11
                    return y;

                },
                DE12: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB12).Value
                    var y = x * this.DC12
                    return y;

                },
                DE13: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB13).Value
                    var y = x * this.DC13
                    return y;

                },
                DE14: function () {
                    debugger
                    var object = [
                        { Name: "Atomizador", Value: this.CF5 },
                        { Name: "Albahaca", Value: this.CF6 },
                        { Name: "Alcohol", Value: this.CF7 },
                        { Name: "Aceite de eucalipto ", Value: this.CF8 },
                        { Name: "Agua", Value: this.CF9 },
                        { Name: "Etiquetas", Value: this.CF10 },
                        { Name: "Bolsa de empaque", Value: this.CF11 },
                    ]
                    // (VLOOKUP(Tabla4[[#This Row],[PRODUCTO]],Tabla1[],6,FALSE)*Tabla4[[#This Row],[CANTIDAD ]],¨ ¨)
                    var x = object.find(x => x.Name == this.DB14).Value
                    var y = x * this.DC14
                    return y;

                },

                DE15: function () {
                    return (
                        this.DE8
                        + this.DE9
                        + this.DE10
                        + this.DE11
                        + this.DE12
                        + this.DE13
                        + this.DE14
                    )
                },
                DE6: function () {
                    if (this.DC6 == 0) return 0
                    return this.DE15 / this.DC6
                },
                EE8: function () {
                    return this.DE6 / (1 - (this.EE20 / 100))
                },
                EI8: function () {
                    return this.EE8 * (this.EE23 / 100)
                },
                EL8: function () {
                    return this.EE8 + this.EI8
                },
                EE15: function () {
                    return this.DE6 * (1 + (this.EE20) / 100)
                },
                EI15: function () {
                    return this.EE15 * (this.EE23 / 100)
                },
                EL15: function () {
                    return this.EE15 + this.EI15
                },
                FB3: function () {
                    return this.G17;
                },
                FB4: function () {
                    return this.DE6;
                },
                FB5: function () {
                    return this.EL15;
                },
                FB6: function () {
                    return this.FB3 / (this.FB5 - this.FB4)
                },
                FB7: function () {
                    return this.FB5 * this.FB6 - this.FB3 - this.FB4 * this.FB6
                },


            },
            methods: {
                formatCurrency(value) {
                    if (typeof value === 'number') {
                        return parseFloat(value.toFixed(2).replace(/\d(?=(\d{3})+\.)/g, '$&.').replace('.', ','));
                    }
                    return '$ 0,00';
                },
                RemoveItem: function (index) {
                    //move the current item to end of collection

                    this.PUNTOArray.splice(index, 1)
                },
                addBusiness: function () {
                    this.PUNTOArray.push({
                        CANTIDAD: (this.PUNTOArray.length > 0) ? (this.PUNTOArray[this.PUNTOArray.length - 1].CANTIDAD) + 1 : 1,
                    });
                },
                DownloadPDF: function () {

                    var doc = new jsPDF();
                    doc.setFontSize(17);
                    var y = 25;
                    // doc.setTextColor(132, 190, 22, 1)
                    doc.text("ESTRUCTURA DE COSTOS", 62, y);

                    doc.setFontSize(10);
                    // y += 9;
                    // doc.setTextColor(100)






                    // doc.text("Sources and Uses", 14, doc.autoTable.previous.finalY + 5);
                    //  y = doc.autoTable.previous.finalY + 6;



                    doc.autoTable({
                        html: '#table1',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 10,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},

                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });
                    doc.autoTable({
                        html: '#table2',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 30,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},

                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });

                    doc.autoTable({
                        html: '#table3',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 24,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });
                    doc.autoTable({
                        html: '#table4',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 34,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });
                    doc.autoTable({
                        html: '#table5',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 10,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var select = $(data.cell.raw).find('select');
                            if (select.length > 0) {
                                // Get the selected option's text
                                var selectedText = select.find('option:selected').text();
                                data.cell.text = selectedText;
                            } else {
                                // If no <select> element is found, keep the cell text as is
                                var inputValue = $(data.cell.raw).find('input').val();
                                data.cell.text = inputValue == undefined ? data.cell.text : inputValue;
                            }
                        }
                    });
                    doc.autoTable({
                        html: '#table6',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 34,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });
                    doc.autoTable({
                        html: '#table7',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 34,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                        }
                    });
                    doc.autoTable({
                        html: '#table8',
                        styles: { cellPadding: 0.1, fontSize: 8 },
                        startY: y += 34,
                        // headStyles :{fillColor : [132, 190, 22]},
                        // footStyles :{fillColor : [132, 190, 22]},
                        didParseCell: function (data) {
                            var x = $(data.cell.raw).find('input').val();
                            data.cell.text = x == undefined ? data.cell.text : x;
                            // Check if the cell is in the last column
                            if (data.column.index === data.table.columns.length - 1) {
                                // If it is the last column, remove the cell text
                                data.cell.text = '';
                            }
                        }
                    });
                    // doc.text("Debt Assumptions", 14, doc.autoTable.previous.finalY + 5);
                    //  y = doc.autoTable.previous.finalY + 6;
                    // doc.autoTable({
                    //     html: '#table3',
                    //     styles: { cellPadding: 0.1, fontSize: 8 },
                    //     startY: y,
                    //     didParseCell: function (data) {
                    //         var x = $(data.cell.raw).find('input').val();
                    //         data.cell.text = x == undefined ? data.cell.text : x;
                    //     }
                    // });
                    // doc.text("SDE Calculation", 14, doc.autoTable.previous.finalY + 5);
                    //  y = doc.autoTable.previous.finalY + 6;
                    // doc.autoTable({
                    //     html: '#table4',
                    //     styles: { cellPadding: 0.1, fontSize: 8 },
                    //     startY: y,
                    //     didParseCell: function (data) {
                    //         var x = $(data.cell.raw).find('input').val();
                    //         data.cell.text = x == undefined ? data.cell.text : x;
                    //     }
                    // });
                    // doc.text("Debt Service Covenant Ratio", 14, doc.autoTable.previous.finalY + 5);
                    //  y = doc.autoTable.previous.finalY + 6;
                    // doc.autoTable({
                    //     html: '#table5',
                    //     styles: { cellPadding: 0.1, fontSize: 8 },
                    //     startY: y,
                    //     didParseCell: function (data) {
                    //         var x = $(data.cell.raw).find('input').val();
                    //         data.cell.text = x == undefined ? data.cell.text : x;
                    //     }
                    // });



                    doc.save('ESTRUCTURA DE COSTOS.pdf');



                },


            },

            components: {
            }
        });
        // vue app
    </script>
</body>

</html>
