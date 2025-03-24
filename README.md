<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Garantia - Gerador</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f4;
        }
        h1 {
            color: #333;
        }
        form {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        label {
            font-weight: bold;
        }
        input[type="text"], input[type="tel"], input[type="date"], textarea, input[type="number"], input[type="file"], input[type="radio"] {
            width: 100%;
            padding: 8px;
            margin: 10px 0;
            border-radius: 4px;
            border: 1px solid #ccc;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .whatsapp-btn {
            background-color: #25D366;
            border-radius: 4px;
            padding: 10px 20px;
            color: white;
            margin-top: 10px;
        }
        .whatsapp-btn:hover {
            background-color: #128C7E;
        }
        .message {
            margin-top: 20px;
            padding: 20px;
            background-color: #f0f8ff;
            border-radius: 8px;
            border: 1px solid #ccc;
            font-size: 18px;
            text-align: center;
            color: #333;
        }
    </style>
</head>
<body>

    <h1>Formulário de Garantia - Gerador</h1>

    <form id="garantia-form">
        <label for="nome">Nome Completo:</label>
        <input type="text" id="nome" name="nome" required><br><br>

        <label for="telefone">Telefone:</label>
        <input type="tel" id="telefone" name="telefone" required><br><br>

        <label for="modelo">Modelo do Gerador:</label>
        <input type="text" id="modelo" name="modelo" required><br><br>

        <label for="problema">Qual é o problema com o gerador?</label><br>
        <textarea id="problema" name="problema" rows="4" required></textarea><br><br>

        <label for="video">Anexe um vídeo do problema (se possível):</label>
        <input type="file" id="video" name="video" accept="video/*"><br><br>

        <label for="solucao">Já tentou alguma solução? Se sim, qual?</label><br>
        <textarea id="solucao" name="solucao" rows="4"></textarea><br><br>

        <label for="data_compra">Data da compra do gerador:</label>
        <input type="date" id="data_compra" name="data_compra" required><br><br>

        <label for="hora_uso">Quantas horas por dia o gerador é utilizado?</label>
        <input type="number" id="hora_uso" name="hora_uso" required><br><br>

        <label for="frequencia_uso">Com que frequência o gerador é utilizado? (Diariamente, Semanalmente, Mensalmente, etc.)</label>
        <input type="text" id="frequencia_uso" name="frequencia_uso" required><br><br>

        <label for="condicoes_armazenamento">Em que condições o gerador é armazenado? (Ex: Ao ar livre, Em ambiente fechado, Etc.)</label><br>
        <textarea id="condicoes_armazenamento" name="condicoes_armazenamento" rows="4" required></textarea><br><br>

        <label for="manutencao">Foi feita alguma manutenção no gerador? Se sim, qual?</label><br>
        <textarea id="manutencao" name="manutencao" rows="4"></textarea><br><br>

        <label for="acessorios">O gerador está acompanhado de algum acessório? (Ex: Manual, Cabos, Chave de Fenda, etc.)</label><br>
        <textarea id="acessorios" name="acessorios" rows="4"></textarea><br><br>

        <label for="marca">Qual é a marca do gerador?</label>
        <input type="text" id="marca" name="marca" required><br><br>

        <label for="problema_repetido">Este problema já ocorreu antes? Se sim, qual a frequência?</label><br>
        <textarea id="problema_repetido" name="problema_repetido" rows="4"></textarea><br><br>

        <label for="tipo_oleo">Qual tipo de óleo você utiliza no gerador?</label>
        <input type="text" id="tipo_oleo" name="tipo_oleo" required><br><br>

        <label for="nivel_oleo">Você já verificou o nível de óleo recentemente? Se sim, qual foi o nível?</label><br>
        <textarea id="nivel_oleo" name="nivel_oleo" rows="4" required></textarea><br><br>

        <label for="troca_oleo">Quando foi a última vez que o óleo foi trocado?</label><br>
        <input type="date" id="troca_oleo" name="troca_oleo" required><br><br>

        <label for="oleo_dentro">O óleo está com coloração normal? (Amarelo, claro, etc.)</label><br>
        <input type="radio" id="oleo_normal" name="oleo_estado" value="Normal">
        <label for="oleo_normal">Normal</label><br>
        <input type="radio" id="oleo_sujo" name="oleo_estado" value="Sujo">
        <label for="oleo_sujo">Sujo (escuro, espesso, etc.)</label><br><br>

        <label for="problemas_oleo">Já notou algum problema relacionado ao óleo? (Ex: vazamento, falta de pressão, etc.)</label><br>
        <textarea id="problemas_oleo" name="problemas_oleo" rows="4"></textarea><br><br>

        <label for="local_uso">Onde o gerador é utilizado? (Ex: Casa, Fazenda, Obra, etc.)</label><br>
        <input type="text" id="local_uso" name="local_uso" required><br><br>

        <label for="temperatura_uso">Em que temperatura o gerador normalmente opera? (Se possível, informe em °C)</label><br>
        <input type="number" id="temperatura_uso" name="temperatura_uso" required><br><br>

        <label for="ruido">O gerador está fazendo mais barulho do que o normal?</label><br>
        <input type="radio" id="ruido_sim" name="ruido" value="Sim">
        <label for="ruido_sim">Sim</label><br>
        <input type="radio" id="ruido_nao" name="ruido" value="Não">
        <label for="ruido_nao">Não</label><br><br>

        <label for="problemas_preexistentes">O gerador já apresentou outros problemas antes deste?</label><br>
        <input type="radio" id="problemas_preexistentes_sim" name="problemas_preexistentes" value="Sim">
        <label for="problemas_preexistentes_sim">Sim</label><br>
        <input type="radio" id="problemas_preexistentes_nao" name="problemas_preexistentes" value="Não">
        <label for="problemas_preexistentes_nao">Não</label><br><br>

        <label for="consumo_combustivel">O consumo de combustível aumentou significativamente?</label><br>
        <input type="radio" id="consumo_sim" name="consumo_combustivel" value="Sim">
        <label for="consumo_sim">Sim</label><br>
        <input type="radio" id="consumo_nao" name="consumo_combustivel" value="Não">
        <label for="consumo_nao">Não</label><br><br>

        <label for="voltagem">Está ocorrendo variação na voltagem do gerador? (Se sim, explique)</label><br>
        <textarea id="voltagem" name="voltagem" rows="4"></textarea><br><br>

        <label for="garantia_documentos">Você tem os documentos de garantia e compra?</label><br>
        <input type="radio" id="garantia_sim" name="garantia_documentos" value="Sim">
        <label for="garantia_sim">Sim</label><br>
        <input type="radio" id="garantia_nao" name="garantia_documentos" value="Não">
        <label for="garantia_nao">Não</label><br><br>

        <button type="button" id="gerar-pdf">Gerar PDF</button>
        <a href="https://wa.me/4896159202?text=Olá,%20preciso%20de%20ajuda%20com%20o%20formulário%20de%20garantia%20do%20gerador.%0A%0ANome:%20" class="whatsapp-btn" target="_blank">Enviar para WhatsApp</a>
    </form>

    <!-- Mensagem sobre a empresa -->
    <div class="message">
        <p><strong>Sobre a DSM Comércio Online:</strong><br>
            A DSM Comércio Online é uma empresa comprometida com a qualidade e confiança em seus produtos e serviços. Sempre oferecendo o melhor para seus clientes, trabalhamos com produtos de alta durabilidade e eficácia, garantindo satisfação e confiança. Estamos prontos para oferecer o melhor atendimento para resolver qualquer problema com os produtos adquiridos em nossa loja. Agradecemos a sua confiança e estamos à disposição para ajudá-lo!</p>
    </div>

    <script>
        document.getElementById('gerar-pdf').addEventListener('click', function() {
            const { jsPDF } = window.jspdf;
            const doc = new jsPDF();

            // Coletando os valores do formulário
            const nome = document.getElementById('nome').value;
            const telefone = document.getElementById('telefone').value;
            const modelo = document.getElementById('modelo').value;
            const problema = document.getElementById('problema').value;
            const video = document.getElementById('video').files[0] ? document.getElementById('video').files[0].name : "Não anexado";
            const solucao = document.getElementById('solucao').value;
            const dataCompra = document.getElementById('data_compra').value;
            const horaUso = document.getElementById('hora_uso').value;
            const frequenciaUso = document.getElementById('frequencia_uso').value;
            const condicoesArmazenamento = document.getElementById('condicoes_armazenamento').value;
            const manutencao = document.getElementById('manutencao').value;
            const acessorios = document.getElementById('acessorios').value;
            const marca = document.getElementById('marca').value;
            const problemaRepetido = document.getElementById('problema_repetido').value;
            const tipoOleo = document.getElementById('tipo_oleo').value;
            const nivelOleo = document.getElementById('nivel_oleo').value;
            const trocaOleo = document.getElementById('troca_oleo').value;
            const oleoEstado = document.querySelector('input[name="oleo_estado"]:checked') ? document.querySelector('input[name="oleo_estado"]:checked').value : "Não informado";
            const problemasOleo = document.getElementById('problemas_oleo').value;
            const localUso = document.getElementById('local_uso').value;
            const temperaturaUso = document.getElementById('temperatura_uso').value;
            const ruido = document.querySelector('input[name="ruido"]:checked') ? document.querySelector('input[name="ruido"]:checked').value : "Não informado";
            const problemasPreexistentes = document.querySelector('input[name="problemas_preexistentes"]:checked') ? document.querySelector('input[name="problemas_preexistentes"]:checked').value : "Não informado";
            const consumoCombustivel = document.querySelector('input[name="consumo_combustivel"]:checked') ? document.querySelector('input[name="consumo_combustivel"]:checked').value : "Não informado";
            const voltagem = document.getElementById('voltagem').value;
            const garantiaDocumentos = document.querySelector('input[name="garantia_documentos"]:checked') ? document.querySelector('input[name="garantia_documentos"]:checked').value : "Não informado";

            // Adicionando o conteúdo ao PDF
            doc.text(`Nome: ${nome}`, 10, 10);
            doc.text(`Telefone: ${telefone}`, 10, 20);
            doc.text(`Modelo: ${modelo}`, 10, 30);
            doc.text(`Problema: ${problema}`, 10, 40);
            doc.text(`Vídeo: ${video}`, 10, 50);
            doc.text(`Solução Tentada: ${solucao}`, 10, 60);
            doc.text(`Data da Compra: ${dataCompra}`, 10, 70);
            doc.text(`Horas de Uso: ${horaUso}`, 10, 80);
            doc.text(`Frequência de Uso: ${frequenciaUso}`, 10, 90);
            doc.text(`Condições de Armazenamento: ${condicoesArmazenamento}`, 10, 100);
            doc.text(`Manutenção: ${manutencao}`, 10, 110);
            doc.text(`Acessórios: ${acessorios}`, 10, 120);
            doc.text(`Marca: ${marca}`, 10, 130);
            doc.text(`Problema Repetido: ${problemaRepetido}`, 10, 140);
            doc.text(`Tipo de Óleo: ${tipoOleo}`, 10, 150);
            doc.text(`Nível de Óleo: ${nivelOleo}`, 10, 170);
            doc.text(`Troca de Óleo: ${trocaOleo}`, 10, 180);
            doc.text(`Estado do Óleo: ${oleoEstado}`, 10, 190);
            doc.text(`Problemas com o Óleo: ${problemasOleo}`, 10, 200);
            doc.text(`Local de Uso: ${localUso}`, 10, 210);
            doc.text(`Temperatura de Uso: ${temperaturaUso}`, 10, 220);
            doc.text(`Ruído: ${ruido}`, 10, 230);
            doc.text(`Problemas Preexistentes: ${problemasPreexistentes}`, 10, 240);
            doc.text(`Consumo de Combustível: ${consumoCombustivel}`, 10, 250);
            doc.text(`Variação de Voltagem: ${voltagem}`, 10, 260);
            doc.text(`Garantia e Documentos: ${garantiaDocumentos}`, 10, 270);

            // Mensagem final sobre a empresa
            doc.text(`\n\nSobre a DSM Comércio Online:\nA DSM Comércio Online é uma empresa comprometida com a qualidade e confiança em seus produtos e serviços. Sempre oferecendo o melhor para seus clientes. Estamos prontos para oferecer o melhor atendimento!`, 10, 280);

            // Salvar o PDF
            doc.save('garantia-gerador.pdf');
        });
    </script>
</body>
</html>
