  <canvas id="myChart" width="400" height="400" bind:this={ctx}></canvas>

<script>
	import { onMount } from 'svelte';
    import Chart from 'chart.js/auto/auto.js';

    let ctx;

    onMount(
        async()=> {
            var myChart = new Shart (ctx, {
                type:'bar',
                data:{
                    labels: [Red, Blue, Yellowe, Green, Purple, orange],
                    datasets:[{
                        labels:'# of Votes',
                        data:[12, 19, 3, 5, 2, 3],
                        backgroundColor: [
                            'rgba (255, 99, 132, 0.2)',
                            'rgba (255, 99, 132, 0.2)',
                            'rgba (255, 99, 132, 0.2)',
                            'rgba (255, 99, 132, 0.2)',
                            'rgba (255, 99, 132, 0.2)',
                        ],
                        borderColor: [
                            'rgba (255, 99,132, 1)',
                            'rgba (255, 99,132, 1)',
                            'rgba (255, 99,132, 1)',
                            'rgba (255, 99,132, 1)',
                            'rgba (255, 99,132, 1)',
                        ],
                        borderWidth: 1
                    }]
                },
                option: {
                    scales:{
                        yAvexs:[{
                            ticks:{
                                beginAtZero:true
                            }
                        }]
                    }
                }
            }) 

        }
    );
</script>


<div>
  <canvas id="myChart"></canvas>
</div>
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