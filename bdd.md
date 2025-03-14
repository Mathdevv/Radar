CREATE DATABASE agenda


-- Estrutura para tabela `horario`


CREATE TABLE `horario` (
  `id_horario` int(11) NOT NULL,
  `DataConsulta` text NOT NULL,
  `Horario` varchar(45) NOT NULL,
  `id_medico` int(11) NOT NULL,
  `id_paciente` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;


-- Despejando dados para a tabela `horario`


INSERT INTO `horario` (`id_horario`, `DataConsulta`, `Horario`, `id_medico`, `id_paciente`) VALUES
(1, 'Sabado', '19:30', 1, 1),
(2, 'Segunda feira', '12:35', 2, 3),
(3, 'Sexta feira', '17:50', 4, 5),
(4, 'Quarta feira', '06:40', 3, 4),
(5, 'Terca feira', '21:00', 5, 2);




-- Estrutura para tabela `medico`


CREATE TABLE `medico` (
  `Id_medico` int(11) NOT NULL,
  `Nome` varchar(45) NOT NULL,
  `SalaMed` decimal(10,0) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;


-- Despejando dados para a tabela `medico`


INSERT INTO `medico` (`Id_medico`, `Nome`, `SalaMed`) VALUES
(1, 'Jorge Lescura', 1),
(2, 'Eduarda Albarelo', 10),
(3, 'Matheus Euphrasio', 3),
(4, 'Rafael Paim', 4),
(5, 'Maria Tereza', 7);




-- Estrutura para tabela `paciente`


CREATE TABLE `paciente` (
  `id_cliente` int(11) NOT NULL,
  `Nome` varchar(45) NOT NULL,
  `DataNasc` date NOT NULL,
  `Genero` char(1) NOT NULL,
  `Cidade` varchar(50) NOT NULL,
  `Historico` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;


-- Despejando dados para a tabela `paciente`


INSERT INTO `paciente` (`id_cliente`, `Nome`, `DataNasc`, `Genero`, `Cidade`, `Historico`) VALUES
(1, 'Julio andrade', '2015-02-09', 'm', 'Cachoeira Paulista', '1'),
(2, 'Roberto Carlos', '2015-03-18', 'm', 'Canas', '2'),
(3, 'Helio Novaes', '2024-08-01', 'm', 'Canas', '3'),
(4, 'Maria Julia', '2018-03-08', 'f', 'Lorena', '4'),
(5, 'Joao Carlos', '2025-03-18', 'm', 'Sao Paulo', '5');


-- Índices de tabela `horario`

ALTER TABLE `horario`
  ADD PRIMARY KEY (`id_horario`);


-- Índices de tabela `medico`

ALTER TABLE `medico`
  ADD PRIMARY KEY (`Id_medico`);


-- Índices de tabela `paciente`

ALTER TABLE `paciente`
  ADD PRIMARY KEY (`id_cliente`) USING BTREE;


-- AUTO_INCREMENT para tabelas despejadas



-- AUTO_INCREMENT de tabela `horario`

ALTER TABLE `horario`
  MODIFY `id_horario` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;


-- AUTO_INCREMENT de tabela `medico`

ALTER TABLE `medico`
  MODIFY `Id_medico` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;


-- AUTO_INCREMENT de tabela `paciente`

ALTER TABLE `paciente`
  MODIFY `id_cliente` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
COMMIT;


