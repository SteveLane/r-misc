## Set graphics device details
.define.fonts <- function(){
    grDevices::quartzFonts(
        raleway = c("Raleway-Light", "Raleway-SemiBold",
                    "Raleway-LightItalic", "Raleway-SemiBoldItalic"),
        opensans = c("OpenSans", "OpenSans-Bold", "OpenSans-Italic",
                     "OpenSans-BoldItalic"))
}
setHook(packageEvent("grDevices", "onLoad"), function(...){
    .define.fonts()
    grDevices::quartz.options(family = "raleway", height = 6, width = 6)
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
