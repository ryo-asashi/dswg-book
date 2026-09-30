options(repos = structure(c(CRAN = "https://cloud.r-project.org/")))
library <- function(...) {
  e <- try(base::library(...), silent = TRUE)
  if (inherits(e, "try-error")) {
    pkg <- as.character(substitute(...))
    install.packages(pkg)
    base::library()
  }
  suppressWarnings(base::library(...))
}