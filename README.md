library(forestplot)
cochrane_from_rmeta <- 
  structure(list(mean  = c(NA, NA, 5.58, 5.83, 3.80, 4.2, 4.98, 3.0, 2.1, 4.25, 5.11, 3.80, 4.90, 4.3, 5.9, 4.5, 5.4, 3, 3.8, NA, 4.38), lower = c(NA, NA, 3.71, 5.23, 2.80, 3.2, 3.73, 2.50, 1.80, 3.67, 4.87, 2.90, 4.3, 3.8, 2.9, 1.8, 3.3, 1.60, 3, NA, 2.8), upper = c(NA,NA, 7.45, 6.43, 4.80, 5.2, 6.23, 3.50, 2.4, 4.83, 5.35, 5, 5.4, 4.8, 11.6, 11.6, 8.6, 4.4, 4.6, NA, 6.45)),.Names = c("mean", "lower", "upper"), row.names = c(NA, -21L), class = "data.frame")

tabletext<-cbind(c("", "Study", "Wara 1973[1]*", "Hornsey 1975[2]*", "Field 1976[3]", "Travis 1983[4]", "Travis 1983[4]", "Parkins 1985[5,6]", "Parkins 1985[5,6]", "Parkins 1985[5-7]*", "Parkins 1985[5-7]*", "Vegesna 1985[8]", "Travis 1987[9]", "Travis 1987[9]", "Travis 1987[10]", "Travis 1987[10]", "Travis 1987[10]", "Van der Kogel 1988[11]*", "Van Rongen et al 1993[12]", NA, "Summary"),
                 c("", "α/β ratio", "5.58", "5.83", "2.80-4.80","4.20", "4.98", "3.00", "2.10", "4.25","5.11", "3.80","4.90", "4.30", "5.90","4.50", "5.40", "3.00", "3.8", NA, "4.38"),  c("", "Endpoint", "LD50", "LD50", "LD50","LD50", "B.R.", "B.R.", "LD50", "B.R.","LD50", "LD50","B.R.", "B.R./LD50", "B.R.","B.R.", "LD50", "ED50", "B.R.", NA, NA))

forestplot(tabletext, cochrane_from_rmeta,new_page = TRUE,graph.pos = 4,hrzl_lines = gpar(col="#444444"),is.summary=c(TRUE, TRUE,rep(FALSE,18),TRUE),boxsize=c(0, 0, 0.3,0.3,0,rep (0.3,15), 1),clip=c(1,12), align = c("l","l"), col=fpColors(box="black",line="black", summary="black"),vertices = TRUE,cex=0,zero=4.38
