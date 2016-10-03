## Set graphics device details
setHook(packageEvent("grDevices", "onLoad"), function(...){
    grDevices::quartz.options(height = 6, width = 6)
})

## For major upgrades, reinstall all packages
.major.upgrades <- function(){
    install.packages(
        lib = lib <- .libPaths()[1],
        pkgs = as.data.frame(installed.packages(lib),
                             stringsAsFactors = FALSE)$Package
    )
}

## Set the repository
local({
  r <- getOption("repos")
  r["CRAN"] <- "https://cran.ms.unimelb.edu.au"
  options(repos = r)
})

## Change digits, stars and strings
options(digits = 3, show.signif.stars = FALSE, stringsAsFactors = FALSE)

## Change printing
options(max.print = 100, scipen = 10)

## Change continue
options(continue = "... ")
