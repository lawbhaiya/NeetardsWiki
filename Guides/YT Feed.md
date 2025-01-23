---
order: 800
icon: triangle-right

---

<div class="video-grid">
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/Al2akzGXsmE?si=y-i-qIOxs5SHE_se" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/-AhEHGYkc9Q?si=8mPmRUGyVYP7pY03" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/43F0MxFRCDE?si=WzNSyv4yMv8fXRAX" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/OOgJU-vMuDY?si=zhagttHKwKfD7sPw" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/yOKosDHgMcM?si=479Jws6Bz-Gucy3R" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/0pJhmRLTSis?si=aR1c4ll7y146Wpxl" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/tlriiUVoK9U?si=XqL1RLW0zmyiFXUo" frameborder="0" allowfullscreen></iframe>
    </div>
    <div class="video-item">
        <iframe src="https://www.youtube.com/embed/cbS7_LAiWaw?si=zgGb00gpXhC9iSNV" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

<div class="pagination">
    <button onclick="prevPage()">1</button>
    <button onclick="nextPage()">2</button>
</div>

<style>
.video-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* Two columns */
    gap: 10px; /* Space between videos */
}

.video-item iframe {
    width: 100%; /* Make the iframe responsive */
    height: 200px; /* Set a fixed height for the videos */
}

.pagination {
    margin-top: 20px;
    text-align: center; /* Center pagination buttons */
}

.pagination button {
    padding: 10px 15px;
    margin: 0 5px;
}
</style>

<script>
let currentPage = 1;
const videosPerPage = 4;

function showVideos() {
    const videoItems = document.querySelectorAll('.video-item');
    const totalVideos = videoItems.length; // Dynamically get total videos
    videoItems.forEach((item, index) => {
        item.style.display = (index >= (currentPage - 1) * videosPerPage && index < currentPage * videosPerPage) ? 'block' : 'none';
    });
}

function nextPage() {
    const totalVideos = document.querySelectorAll('.video-item').length; // Recalculate total videos
    if (currentPage * videosPerPage < totalVideos) {
        currentPage++;
        showVideos();
    }
}

function prevPage() {
    if (currentPage > 1) {
        currentPage--;
        showVideos();
    }
}

// Initial call to display videos
showVideos();
</script>
