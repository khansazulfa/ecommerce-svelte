<script>
  import { Row, Col, ListGroupItem } from "sveltestrap";
//Props
  export let produk = "Tidak ada merk";
  export let desc = "Tidak ada deskripsi";

</script>

<ListGroupItem>
    <Row>
        <Col>
            <img src="image/foto-produk.png" alt="foto produk" width="100"/>
        </Col>
        <Col>
            <h5>{produk}</h5>
            <p>{desc}</p>
        </Col>
    </Row>
</ListGroupItem>
