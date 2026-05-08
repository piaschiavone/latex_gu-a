# latex_guia
Cómo usar latex
% ============================================================
%  GUÍA PRÁCTICA DE LaTeX
%  Compilar con: pdflatex archivo.tex
% ============================================================

\documentclass[12pt, a4paper]{article}  % Tipo de documento

% ── PAQUETES ESENCIALES ──────────────────────────────────────
\usepackage[utf8]{inputenc}       % Soporte para tildes y ñ
\usepackage[spanish]{babel}       % Idioma español
\usepackage{amsmath, amssymb}     % Matemáticas avanzadas
\usepackage{graphicx}             % Imágenes
\usepackage{hyperref}             % Links clicables
\usepackage{geometry}             % Márgenes
\geometry{margin=2.5cm}

% ── METADATOS DEL DOCUMENTO ──────────────────────────────────
\title{Mi Primer Documento en \LaTeX}
\author{Tu Nombre}
\date{\today}                     % Fecha automática

% ============================================================
\begin{document}
% ============================================================

\maketitle          % Genera el título automáticamente
\tableofcontents    % Índice automático
\newpage

% ── SECCIONES ────────────────────────────────────────────────
\section{Introducción}
LaTeX separa el \textbf{contenido} del \textit{formato}.
Escribís el texto y LaTeX se encarga del diseño.

\subsection{¿Por qué usarlo?}
\begin{itemize}
    \item Documentos de calidad tipográfica profesional
    \item Ideal para fórmulas matemáticas
    \item Manejo automático de referencias, índices y bibliografía
    \item Gratuito y multiplataforma
\end{itemize}

\subsection{¿Cuándo NO usarlo?}
\begin{enumerate}
    \item Cuando el diseño visual es lo principal
    \item Para documentos simples sin estructura compleja
    \item Cuando necesitás resultados muy rápidos sin aprender sintaxis
\end{enumerate}

% ── TEXTO ────────────────────────────────────────────────────
\section{Formato de Texto}

\textbf{Negrita} \quad \textit{Cursiva} \quad \underline{Subrayado}
\quad \texttt{Monoespaciado (código)}

% Salto de párrafo: línea en blanco en el fuente
Este es el primer párrafo.

Este es el segundo párrafo. LaTeX ajusta los espacios solo.

% ── MATEMÁTICAS ──────────────────────────────────────────────
\section{Matemáticas}

% Inline (dentro del texto):
La fórmula de Euler es $e^{i\pi} + 1 = 0$, considerada la más bella.

% Bloque centrado:
\[
    \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
\]

% Ecuaciones numeradas y alineadas:
\begin{align}
    f(x)  &= x^2 + 3x - 4       \\
    f'(x) &= 2x + 3              \\
    f(2)  &= 4 + 6 - 4 = 6
\end{align}

% Fracciones, raíces, matrices:
\[
    \frac{a+b}{c} \quad \sqrt[3]{8} = 2 \quad
    \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}
\]

% ── TABLAS ───────────────────────────────────────────────────
\section{Tablas}

\begin{table}[h]
    \centering
    \caption{Comparación de herramientas}
    \begin{tabular}{|l|c|c|}
        \hline
        \textbf{Herramienta} & \textbf{Fórmulas} & \textbf{Fácil} \\
        \hline
        LaTeX   & Excelente & No   \\
        Word    & Regular   & Sí   \\
        Markdown & Básico   & Sí   \\
        \hline
    \end{tabular}
    \label{tab:comparacion}
\end{table}

% ── IMÁGENES ─────────────────────────────────────────────────
\section{Imágenes}

\begin{figure}[h]
    \centering
    \includegraphics[width=0.5\textwidth]{mi_imagen.png}
    \caption{Descripción de la imagen}
    \label{fig:ejemplo}
\end{figure}

% Referencia cruzada automática: ver Figura~\ref{fig:ejemplo}

% ── REFERENCIAS ──────────────────────────────────────────────
\section{Referencias cruzadas y citas}

Como se muestra en la Tabla~\ref{tab:comparacion}, LaTeX destaca
en fórmulas. La ecuación~\ref{eq:pitagoras} es conocida:

\begin{equation}
    a^2 + b^2 = c^2
    \label{eq:pitagoras}
\end{equation}

% ── BIBLIOGRAFÍA ─────────────────────────────────────────────
\begin{thebibliography}{9}
    \bibitem{lamport94}
        Leslie Lamport,
        \textit{LaTeX: A Document Preparation System},
        Addison-Wesley, 1994.
\end{thebibliography}

\end{document}
