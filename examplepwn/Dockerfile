FROM ubuntu:latest

# Salin file soal ke dalam direktori / di dalam wadah
COPY soal /

# Berikan izin eksekusi ke file soal
RUN chmod +x /soal

# Instal socat di dalam wadah
RUN apt-get update && apt-get install -y socat

# Expose port 1001
EXPOSE 1001

# Atur perintah untuk menjalankan socat dan eksekusi soalram soal
CMD ["socat", "TCP-LISTEN:1001,fork", "EXEC:/soal"]

