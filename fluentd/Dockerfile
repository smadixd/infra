FROM fluent/fluentd:edge-debian

# Install Fluentd Prometheus plugin
RUN gem install fluent-plugin-prometheus --no-document

# Set environment variable for Fluentd config
ENV FLUENTD_CONF=fluentd.conf

# Copy Fluentd configuration file
COPY fluentd.conf /fluentd/etc/fluentd.conf

# Expose Fluentd and Prometheus ports
EXPOSE 24224 24231

# Run Fluentd command by default
CMD fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins