# B4-T02---M-DULOS-E-DESIGN-PATTERNS

<!DOCTYPE html>
<html lang="pt_br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Formulários de Cadastro e Relatório</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f2f2f2;
        margin: 0;
        padding: 0;
    }

    .container {
        background-color: #ffffff;
        width: 80%;
        max-width: 600px;
        margin: 20px auto;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    .header {
        text-align: center;
        background-color: #007BFF;
        color: #fff;
        padding: 10px;
        border-radius: 8px 8px 0 0;
    }

    h3 {
        text-align: center;
        font-size: 24px;
        color: #007BFF;
    }

    p {
        text-align: center;
        font-size: 18px;
        color: #333;
    }

    table {
        width: 100%;
    }

    td {
        padding: 10px;
    }

    input[type="text"] {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
    }

    .btn {
        background-color: #007BFF;
        color: #fff;
        padding: 10px 20px;
        border: none;
        cursor: pointer;
        border-radius: 5px;
    }

    .btn:hover {
        background-color: #0056b3;
    }
</style>
</head>
<body>
<div class="container">
    <div class="header">
        <h3>:::::::::::::::::::::::::::::::::: BEM VINDO AO SISTEMA ::::::::::::::::::::::::::</h3>
        <p> ::::::::::::::::::::::::::::::::::CADASTRO DE CIDADES E ESTADOS :::::::::::::::::::::::::::::::::::::::::::</p>
    </div>
    <form action="conexao.php" method="POST">
        <table>
            <tr>
                <td>CIDADE:</td>
                <td><input id="cidade" maxlength="100" name="cidade" size="40" type="text" /></td>
            </tr>
            <tr>
                <td>ESTADO:</td>
                <td><input id="uf" maxlength="2" name="sigla" size="2" type="text" /></td>
            </tr>
            <tr>
                <td>ID:</td>
                <td><input id="id" name="id" type="text" /></td>
            </tr>
            <tr>
                <td colspan="2">
                    <p>
                        <input class="btn" type="submit" value="CADASTRAR/ATUALIZAR" />
                    </p>
                </td>
            </tr>
        </table>
    </form>
    <br>
    <form action="gerar_relatorio.php" method="post" target="_blank">
        <label for="opcao">Escolha a opção de relatório:</label>
        <select name="opcao" id="opcao">
            <option value="cidades">Somente Cidades</option>
            <option value="estados">Somente Estados</option>
            <option value="cidades_por_estados">Cidades por Estados</option>
        </select>
        <input type="submit" class="btn" value="Gerar Relatório" />
    </form>
    <br>
    <form action="excluir_registro.php" method="POST">
        <table>
            <tr>
                <td>ID para Exclusão:</td>
                <td><input id="id" name="id" type="text" /></td>
            </tr>
            <tr>
                <td colspan="2">
                    <p>
                        <input class="btn" type="submit" value="EXCLUIR" />
                    </p>
                </td>
            </tr>
        </table>
    </form>
</div>
</body>
</html>
