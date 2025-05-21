## OpenAQ GMU InSitu API Endpoints

### Below are the details of the InSitu API endpoints to get sensor and reading data.
<table>
  <tr>
    <th>Processing Level</th>
    <th>Endpoint</th>
    <th>Required Variables</th>
    <th>Optional Variables</th>
    <th>Default Values</th>
    <th>Constraints</th>
  </tr>

  <tr>
    <td rowspan="5">Hourly</td>
    <td>sensor_data_openaq</td>
    <td>date, min_lon, max_lon, min_lat, max_lat, processing_level</td>
    <td>variable (pm2_5, temperature, humidity)</td>
    <td>
      <ul>
        <li>variable: pm2_5</li>
        <li>provider: Clarity</li>
      </ul>
    </td>
    <td>No specific constraints</td>
  </tr>

  <tr>
    <td colspan="5"><strong>Sample Request:</strong> 
      <a href="https://insitu-api.stcenter.net/sensor_data_openaq?date=2024-01-12&variable=pm2_5&min_lon=-123.0&max_lon=-122.0&min_lat=37.0&max_lat=38.0&provider=Clarity&processing_level=hourly" target="_blank">
        https://insitu-api.stcenter.net/sensor_data_openaq?...
      </a>
    </td>
  </tr>

  <tr>
    <td>activities_openaq</td>
    <td>sensor_ids, sd (start date), ed (end date), provider, processing_level</td>
    <td></td>
    <td></td>
    <td>      
      <ul>
          <li>Maximum of 500 sensors allowed per request.</li>
          <li>An end date is mandatory for each request.</li>
          <li>The time span between the start date and end date must not exceed 7 days.</li>
      </ul></td>
  </tr>
    <tr>
    <td colspan="5"><strong>Sample Request:</strong>
      <a href="https://insitu-api.stcenter.net/activities_openaq?sd=2024-01-12&ed=2024-01-13&sensor_ids=2001417,4448663,2001466,2001397&provider=Clarity&processing_level=hourly" target="_blank">
        https://insitu-api.stcenter.net/activities_openaq?sd=2024-01-12....
      </a>
    </td>
  </tr>

   <tr>
    <td>training_data_openaq</td>
    <td>state_code, county_code, provider, target</td>
    <td>distance, corr_threshold, type</td>
    <td>
      <ul>
        <li>provider: Clarity</li>
        <li>target: Airnow</li>
        <li>corr_threshold: 0.4</li>
        <li>type: csv</li>
      </ul>
    </td>
    <td>No specific constraints</td>
  </tr>

</table>

### This API endpoint is used to retrieve training data for calibration modeling.
<table>
  <tr>
    <th>Endpoint</th>
    <th>Required Variables</th>
    <th>Optional Variables</th>
    <th>Default Values</th>
    <th>Constraints</th>
  </tr>

  <tr>
    <td>training_data_openaq</td>
    <td>state_code, county_code, provider, target</td>
    <td>distance, corr_threshold, type</td>
    <td>
      <ul>
        <li>provider: Clarity</li>
        <li>target: Airnow</li>
        <li>corr_threshold: 0.4</li>
        <li>type: csv</li>
      </ul>
    </td>
    <td>No specific constraints</td>
  </tr>

  <tr>
    <td colspan="5"><strong>Sample Request:</strong><br>
      <a href="https://insitu-api.stcenter.net/training_data_openaq?state_code=06&county_code=001&distance=5000&type=csv&provider=Clarity&corr_threshold=0.4&target=Airnow" target="_blank">
        https://insitu-api.stcenter.net/training_data_openaq?...
      </a>
    </td>
  </tr>
</table>

