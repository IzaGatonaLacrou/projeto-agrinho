# projeto-agrinho
// Exemplo de código para um irrigador automático simples

// Função para simular a ativação da irrigação
function ativarIrrigacao() {
    console.log("Irrigação ativada!");
    // Aqui você colocaria o código para ligar as válvulas ou enviar comandos para hardware real
}

// Função para desativar a irrigação
function desativarIrrigacao() {
    console.log("Irrigação desativada!");
    // Aqui você colocaria o código para desligar as válvulas ou enviar comandos para hardware real
}

// Função para verificar se é hora de ativar a irrigação (exemplo simples baseado em horário)
function verificarHoraIrrigacao() {
    // Obter a hora atual
    const agora = new Date();
    const horaAtual = agora.getHours();
    
    // Definir o horário de início e fim da irrigação (exemplo: das 8h às 18h)
    const horaInicio = 8;
    const horaFim = 18;
    
    // Verificar se a hora atual está dentro do intervalo de irrigação
    if (horaAtual >= horaInicio && horaAtual < horaFim) {
        ativarIrrigacao();
    } else {
        desativarIrrigacao();
    }
}

// Função para simular a verificação periodicamente (a cada minuto, por exemplo)
function iniciarVerificacaoPeriodica() {
    verificarHoraIrrigacao();
    setInterval(verificarHoraIrrigacao, 60000); // Verifica a cada 1 minuto (60000 milissegundos)
}

// Iniciar verificação periódica ao carregar o script (simulação)
iniciarVerificacaoPeriodica();
