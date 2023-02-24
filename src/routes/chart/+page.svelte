 <canvas id="myChart" width="400" height="400"></canvas>

<script>

    import { onMount } from 'svelte';

    function createChart () {       

    var ctx = document.getElementById('myChart');
    var myChart = new Chart(ctx, {
        type: 'bar',
            data: {
                labels: [ 'Apple', 'Orange', 'Strawberry' ],
                datasets: [{
                label: '# of Votes',
                data: [12, 19, 7],
                backgroundColor: [
                    'rgba(255, 99, 132, 0.2)',
                    'rgba(54, 162, 235, 0.2)',
                    'rgba(255, 206, 86, 0.2)'
                    ],
                borderColor: [
                    'rgba(255, 99, 132, 1)',
                    'rgba(54, 162, 235, 1)',
                    'rgba(255, 206, 86, 1)'
                    ],
                borderWidth: 1
            }]
        },
            options: {
                scales: {
                y: {
                beginAtZero: true
                }
            }
        }
    });
}
onMount(createChart);
</script>



<h3>Shopping Bag</h3>

<div class="shopping-bag">
    <table>
        <thead>
            <tr>
                <th>Produk Terpilih</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>produk</td>
            </tr>
        </tbody>
    </table>
</div>

<style>
    h3{
        text-align: center;
    }
table, td, th {
    border: 1px solid #a5a5a5;
    height: 50px;
}

table {
    border-collapse: collapse;
    width: 100%;
}
</style>