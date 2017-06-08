## Set graphics device details
setHook(packageEvent("grDevices", "onLoad"), function(...){
    grDevices::quartzFonts(
                   mono = paste0("Hack-",
                                 c("Regular", "Bold", "Italic", "BoldItalic")))
    grDevices::quartz.options(height = 6, width = 6, family = "mono")
})
setHook(packageEvent("Cairo", "onLoad"), function(...){
    Cairo::CairoFonts(
               regular="Hack:style=Regular",
               bold="Hack:style=Bold",
               italic="Hack:style=Italic",
               bolditalic="Hack:style=BoldItalic",
               symbol="Symbol"
           )
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
  r["CRAN"] <- "https://cran.csiro.au/"
  options(repos = r)
})

## Change digits, stars and strings
options(digits = 3, show.signif.stars = FALSE, stringsAsFactors = FALSE)

## Change printing
options(max.print = 1000, scipen = 10)
