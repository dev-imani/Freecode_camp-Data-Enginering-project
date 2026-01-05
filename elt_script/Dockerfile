FROM python:3.8-slim

# Install PostgreSQL command-line tools (match server major version 15)
RUN apt-get update \
    && apt-get install -y postgresql-client-15 \
    && rm -rf /var/lib/apt/lists/*

# Copy the ELT script 
COPY elt_script.py .

# Set the default command to run the ELT script
CMD ["python", "elt_script.py"]