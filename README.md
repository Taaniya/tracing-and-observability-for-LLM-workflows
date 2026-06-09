Different open source frameworks for tracing & observability -
1. [MLFlow](https://mlflow.org/docs/latest/tracing/ui)
2. [OpenTelemetry](https://opentelemetry.io/docs/concepts/signals/traces/)
3. [LangFuse](https://langfuse.com/)
4. [Arize AI - Phoenix](https://arize.com/docs/phoenix/tracing/llm-traces) - AI observability and evaluation
5. [TruLens](https://www.trulens.org/component_guides/instrumentation/)
6. [Jaeger](https://www.jaegertracing.io/)


# 1. Tracing with MLFlow

**Set up -**
1. install mlflow in your env
   ```
   pip install mlflow
   ```
2. Launch mlflow UI
   ```
   mlflow ui
   ```

3. Add following lines in your code -
   ```
   import mlflow
   mlflow.set_tracking_uri('http://localhost:5000')
   mlflow.litellm.autolog()
   ```
  Note: The tracking URL is the same URL at which the mlflow server ui is launched -
  ![image1](mlflow_tracer.png)


**References –**
* https://mlflow.org/docs/latest/tracing/ui
* https://mlflow.org/docs/latest/tracing
* https://mlflow.org/docs/latest/tracking/server/
* https://mlflow.org/docs/latest/tracing/api/search


# 2. Phoenix 
* Setup (self-hosting) -
  
   install phoenix tracing library in your local
   ```
   pip install arize-phoenix
   ```
   start phoenix
  ```
  phoenix serve
  ```
**References -**
  * Send traces from your app - https://arize.com/docs/phoenix/get-started/get-started-tracing
  * Also Supports self-hosting - https://arize.com/docs/phoenix/self-hosting/deployment-options/terminal
  * Enable tracing from google-adk agentic flows - https://arize.com/docs/phoenix/integrations/python/google-adk/google-adk-tracing
*  Cookbooks - https://arize.com/docs/phoenix/cookbook
*  Log evaluations - https://arize.com/docs/phoenix/tracing/how-to-tracing/feedback-and-annotations/llm-evaluations





