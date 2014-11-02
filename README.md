#' Building a model with top 10 featues
#' 
#' This function develops a prediction algorithm based on the top 
#' 10 features in x that are most predicative of y.
#' 
#' @param x a n x p matrix of n observations and p predictors
#' @param y a vector of length n representing the response
#' @return a vector of coefficients from the final fitted model with top 10 features
#' @author Eric Dolan
#' @details This function rurns a univariate regression of y on each predictor in x and 
#' calculates a p-value indicating the significance of the association.
#' The final set of 10 predictors is taken from the 10 smallest pvalues.
#' @seealso \code{lm}
#' @export
#' @importFrom stats lm