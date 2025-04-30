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
    <td rowspan="3">Hourly</td>
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
    <td>activities (In progress)</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
