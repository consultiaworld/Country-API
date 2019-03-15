# Country-API

/* This app doesn't follow a11y best practices, and the JS file is incomplete. Complete the getDataFromApi and displaySearchData functions. When you're done, this app should allow a user to search for a country, and display the name of that country, followed by a list of the country's population, capital and region. You should make requests to this API: https://restcountries.eu/ . Also make any necessary adjustments to make this app accessible. */

'use strict'

const baseURL = "https://restcountries.eu/rest/v2/name/"

function getDataFromApi(searchTerm, callback) {
  let countryURL = baseURL + 
  // your code here
}

function displaySearchData(data) {
  // your code here
}

function watchSubmit() {
  $('.js-search-form').submit(event => {
    event.preventDefault();
    let queryTarget = $(event.currentTarget).find('.js-query');
    let query = queryTarget.val();
    // clear out the input
    queryTarget.val("");
    getDataFromApi(query, displaySearchData);
  });
}

$(watchSubmit);
