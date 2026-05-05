# Graph Report - .  (2026-05-05)

## Corpus Check
- Large corpus: 475 files · ~1,007,135 words. Semantic extraction will be expensive (many Claude tokens). Consider running on a subfolder, or use --no-semantic to run AST-only.

## Summary
- 7309 nodes · 71930 edges · 86 communities detected
- Extraction: 15% EXTRACTED · 85% INFERRED · 0% AMBIGUOUS · INFERRED: 61178 edges (avg confidence: 0.51)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Canned Responses & Data Models|Canned Responses & Data Models]]
- [[_COMMUNITY_Alpha Engine & Guideline Matching|Alpha Engine & Guideline Matching]]
- [[_COMMUNITY_DTO Mappings & Configuration|DTO Mappings & Configuration]]
- [[_COMMUNITY_Prompt Engineering & Drafting|Prompt Engineering & Drafting]]
- [[_COMMUNITY_Policies & Perceived Performance|Policies & Perceived Performance]]
- [[_COMMUNITY_Response Generation & No-Match Handling|Response Generation & No-Match Handling]]
- [[_COMMUNITY_System Health & Monitoring|System Health & Monitoring]]
- [[_COMMUNITY_Session & Entity Management|Session & Entity Management]]
- [[_COMMUNITY_SDK & API Validation Tests|SDK & API Validation Tests]]
- [[_COMMUNITY_Journey & Guideline Integration|Journey & Guideline Integration]]
- [[_COMMUNITY_Community 10|Community 10]]
- [[_COMMUNITY_Community 11|Community 11]]
- [[_COMMUNITY_Community 12|Community 12]]
- [[_COMMUNITY_Community 13|Community 13]]
- [[_COMMUNITY_Community 14|Community 14]]
- [[_COMMUNITY_Community 15|Community 15]]
- [[_COMMUNITY_Community 16|Community 16]]
- [[_COMMUNITY_Community 17|Community 17]]
- [[_COMMUNITY_Community 19|Community 19]]
- [[_COMMUNITY_Community 20|Community 20]]
- [[_COMMUNITY_Community 21|Community 21]]
- [[_COMMUNITY_Community 22|Community 22]]
- [[_COMMUNITY_Community 23|Community 23]]
- [[_COMMUNITY_Community 24|Community 24]]
- [[_COMMUNITY_Community 26|Community 26]]
- [[_COMMUNITY_Community 27|Community 27]]
- [[_COMMUNITY_Community 28|Community 28]]
- [[_COMMUNITY_Community 29|Community 29]]
- [[_COMMUNITY_Community 30|Community 30]]
- [[_COMMUNITY_Community 31|Community 31]]
- [[_COMMUNITY_Community 32|Community 32]]
- [[_COMMUNITY_Community 33|Community 33]]
- [[_COMMUNITY_Community 35|Community 35]]
- [[_COMMUNITY_Community 36|Community 36]]
- [[_COMMUNITY_Community 37|Community 37]]
- [[_COMMUNITY_Community 38|Community 38]]
- [[_COMMUNITY_Community 40|Community 40]]
- [[_COMMUNITY_Community 44|Community 44]]
- [[_COMMUNITY_Community 45|Community 45]]
- [[_COMMUNITY_Community 47|Community 47]]
- [[_COMMUNITY_Community 48|Community 48]]
- [[_COMMUNITY_Community 51|Community 51]]
- [[_COMMUNITY_Community 52|Community 52]]
- [[_COMMUNITY_Community 55|Community 55]]
- [[_COMMUNITY_Community 60|Community 60]]
- [[_COMMUNITY_Community 62|Community 62]]
- [[_COMMUNITY_Community 63|Community 63]]
- [[_COMMUNITY_Community 64|Community 64]]
- [[_COMMUNITY_Community 91|Community 91]]
- [[_COMMUNITY_Community 92|Community 92]]
- [[_COMMUNITY_Community 93|Community 93]]
- [[_COMMUNITY_Community 94|Community 94]]
- [[_COMMUNITY_Community 95|Community 95]]
- [[_COMMUNITY_Community 96|Community 96]]
- [[_COMMUNITY_Community 97|Community 97]]
- [[_COMMUNITY_Community 104|Community 104]]
- [[_COMMUNITY_Community 106|Community 106]]
- [[_COMMUNITY_Community 107|Community 107]]
- [[_COMMUNITY_Community 108|Community 108]]
- [[_COMMUNITY_Community 109|Community 109]]
- [[_COMMUNITY_Community 110|Community 110]]
- [[_COMMUNITY_Community 111|Community 111]]
- [[_COMMUNITY_Community 114|Community 114]]
- [[_COMMUNITY_Community 141|Community 141]]
- [[_COMMUNITY_Community 142|Community 142]]
- [[_COMMUNITY_Community 143|Community 143]]
- [[_COMMUNITY_Community 144|Community 144]]
- [[_COMMUNITY_Community 145|Community 145]]
- [[_COMMUNITY_Community 146|Community 146]]
- [[_COMMUNITY_Community 147|Community 147]]
- [[_COMMUNITY_Community 148|Community 148]]
- [[_COMMUNITY_Community 149|Community 149]]
- [[_COMMUNITY_Community 150|Community 150]]
- [[_COMMUNITY_Community 151|Community 151]]
- [[_COMMUNITY_Community 152|Community 152]]
- [[_COMMUNITY_Community 153|Community 153]]
- [[_COMMUNITY_Community 154|Community 154]]
- [[_COMMUNITY_Community 155|Community 155]]
- [[_COMMUNITY_Community 156|Community 156]]
- [[_COMMUNITY_Community 157|Community 157]]
- [[_COMMUNITY_Community 158|Community 158]]
- [[_COMMUNITY_Community 159|Community 159]]
- [[_COMMUNITY_Community 160|Community 160]]
- [[_COMMUNITY_Community 161|Community 161]]
- [[_COMMUNITY_Community 162|Community 162]]
- [[_COMMUNITY_Community 163|Community 163]]

## God Nodes (most connected - your core abstractions)
1. `Logger` - 1125 edges
2. `Tracer` - 878 edges
3. `Meter` - 827 edges
4. `PromptBuilder` - 746 edges
5. `DefaultBaseModel` - 727 edges
6. `GuidelineMatch` - 699 edges
7. `ToolId` - 656 edges
8. `ItemNotFoundError` - 632 edges
9. `Tag` - 613 edges
10. `Embedder` - 612 edges

## Surprising Connections (you probably didn't know these)
- `create_guideline()` --calls--> `ToolId`  [INFERRED]
  tests/test_utilities.py → src/parlant/core/tools.py
- `logger()` --calls--> `StdoutLogger`  [INFERRED]
  tests/conftest.py → src/parlant/core/loggers.py
- `configure_module()` --calls--> `PluginServer`  [INFERRED]
  tests/modules/bank.py → src/parlant/core/services/tools/plugins.py
- `list_categories()` --calls--> `ToolResult`  [INFERRED]
  tests/modules/tech_store.py → src/parlant/core/tools.py
- `Test latch behavior when task is cancelled but latch suppresses it.` --uses--> `CancellationSuppressionLatch`  [INFERRED]
  tests/core/test_cancellation_suppression_latch.py → src/parlant/core/async_utils.py

## Hyperedges (group relationships)
- **NLP Service Components** — custom_llms_nlp_service, custom_llms_schematic_generator, custom_llms_embedder, custom_llms_moderation_service [EXTRACTED 1.00]
- **Agent Configuration Entities** — readme_agent, readme_guideline, readme_journey, readme_tool, readme_canned_response [EXTRACTED 1.00]
- **Session Event Structure** — sessions_session, sessions_event, sessions_trace_id [EXTRACTED 1.00]
- **Prompt Construction Flow** — builder_diagram, agent_context_diagram, context_variable_diagram, glossary_diagram [EXTRACTED 0.90]
- **Guideline Engine Components** — guideline_matcher_diagram, guideline_match_diagram, previously_applied_actionable_bat_match_diagram [EXTRACTED 0.85]
- **Inference Pipeline** — inference_data_diagram, inference_result_diagram, tool_caller_diagram, tool_insight_diagram [EXTRACTED 0.80]
- **NLP Infrastructure** — generation_streamingtextgenerator, generation_schematicgenerator, tokenization_estimatingtokenizer [EXTRACTED 1.00]
- **Core Matching Engine** — guideline_matcher_guidelinematcher, tool_caller_toolcaller, generic_guideline_previously_applied_actionable_batch_genericpreviouslyappliedactionablebatch [INFERRED 0.90]
- **NLP Service Components** — custom_llms_schematic_generator, custom_llms_embedder, custom_llms_moderation_service [EXTRACTED 1.00]
- **Engine Customization Mechanics** — engine_extensions_engine_hooks, engine_extensions_dependency_injection, custom_llms_nlp_service [INFERRED 0.90]
- **Parlant Governance Stack** — api_hardening_authorization_policy, api_hardening_rate_limiter, input_moderation_content_filtering [INFERRED 0.85]
- **Core Conversational Entities** — motivation_guideline, installation_journey, installation_tool, installation_canned_response [EXTRACTED 0.95]

## Communities

### Community 0 - "Canned Responses & Data Models"
Cohesion: 0.01
Nodes (911): ABC, AdditionalFieldExtraction, CannedResponseContext, CannedResponseDraftSchema, CannedResponseFieldExtractionMethod, CannedResponseFieldExtractionSchema, CannedResponseFieldExtractor, CannedResponseGeneratorDraftShot (+903 more)

### Community 1 - "Alpha Engine & Guideline Matching"
Cohesion: 0.01
Nodes (684): BasicPlan, do_create_plan(), do_on_guidelines_matched(), do_on_guidelines_resolved(), do_on_tools_called(), do_on_tools_inferred(), Base plan with built-in tracing and logger scoping.      Derived classes impleme, Base planner with built-in tracing and logger scoping.      Derived classes impl (+676 more)

### Community 2 - "DTO Mappings & Configuration"
Cohesion: 0.01
Nodes (676): _dto_to_canned_response_field(), composition_mode_dto_to_composition_mode(), composition_mode_to_composition_mode_dto(), CompositionModeDTO, EvaluationStatusDTO, GuidelineContentDTO, GuidelineDTO, GuidelinePayloadOperationDTO (+668 more)

### Community 3 - "Prompt Engineering & Drafting"
Cohesion: 0.01
Nodes (470): _get_response_template_fields(), get_template(), AlphaEngine, empty(), IterationState, last_customer_message(), messages(), ResponseState (+462 more)

### Community 4 - "Policies & Perceived Performance"
Cohesion: 0.01
Nodes (449): Determines if messages should be split into multiple parts.          :param cont, A default implementation of the perceived performance policy that uses reasonabl, An interface for defining perceived performance policies for the engine., Provides perceived performance policies on a per-agent basis., Returns the perceived performance policy for the given agent.          :param ag, Sets the perceived performance policy for the given agent.          :param agent, Returns the delay before the indicator (agent is thinking...) is sent., Returns the delay before the indicator (agent is thinking "hard"...) is sent. (+441 more)

### Community 5 - "Response Generation & No-Match Handling"
Cohesion: 0.19
Nodes (336): BasicNoMatchResponseProvider, CannedResponseGenerator, NoMatchResponseProvider, PreambleConfiguration, EngineContext, Interaction, InteractionMessage, EntityContext (+328 more)

### Community 6 - "System Health & Monitoring"
Cohesion: 0.01
Nodes (172): configure_healthz(), Build SchemaThresholds from seconds for readability., Configure the ``HealthReporter`` for the ``/healthz`` response.      Sets up ret, _t(), test_event_loop_monitor_detects_degraded_loop(), test_event_loop_monitor_detects_unhealthy_loop(), test_that_draining_queued_messages_without_subscribers_does_not_starve_event_loop(), check_required_schema_migrations() (+164 more)

### Community 7 - "Session & Entity Management"
Cohesion: 0.02
Nodes (177): agent_id(), customer_id(), session_id(), event_is_according_to_params(), get_cow_uttering(), long_session_id(), make_event_params(), populate_session_id() (+169 more)

### Community 8 - "SDK & API Validation Tests"
Cohesion: 0.03
Nodes (98): test_that_action_proposition_is_evaluated(), run_cli(), run_cli_and_get_exit_status(), test_that_a_customer_can_be_added(), test_that_a_customer_can_be_deleted(), test_that_a_customer_can_be_updated(), test_that_a_customer_can_be_viewed(), test_that_a_customer_metadata_can_be_set() (+90 more)

### Community 9 - "Journey & Guideline Integration"
Cohesion: 0.03
Nodes (39): format_journey_node_guideline_id(), anthropic(), azure(), cerebras(), _create_field_provider_shim(), _create_guideline_handler_shim(), _create_journey_state_handler_shim(), current() (+31 more)

### Community 10 - "Community 10"
Cohesion: 0.04
Nodes (40): make_request(), test_that_a_configured_operation_is_limited_per_minute(), test_that_limits_are_isolated_per_client_ip(), test_that_limits_are_isolated_per_operation_bucket(), test_that_missing_client_ip_raises_authorization_exception(), test_that_x_forwarded_for_overrides_request_client_host_for_ip_selection(), addItemToIndexedDB(), cn() (+32 more)

### Community 11 - "Community 11"
Cohesion: 0.06
Nodes (19): _get_staged_events(), _get_tool_calls(), _has_status_event(), then_a_cancelled_status_event_is_emitted(), then_a_processing_status_event_is_emitted(), then_a_ready_status_event_is_emitted(), then_a_single_event_is_staged(), then_a_single_message_event_is_emitted() (+11 more)

### Community 12 - "Community 12"
Cohesion: 0.12
Nodes (19): install_package(), lint_package(), run_cmd_or_die(), get_server_version(), publish_docker(), publish_package(), run_command(), die() (+11 more)

### Community 13 - "Community 13"
Cohesion: 0.08
Nodes (27): Probabilistic Behavior, AuthorizationPolicy, Rate Limiter, Hexagonal Architecture, parlant-chat-react, Parlant Chat Interface, Attentive Reasoning Queries (ARQs), Manual Mode (+19 more)

### Community 14 - "Community 14"
Cohesion: 0.15
Nodes (12): hasOtherOpenedTabs(), setLogsFn(), checkAndCleanupLogs(), deleteOldestLogs(), getAgentMessageLogsCount(), getAllLogKeys(), getLogs(), getMessageLogs() (+4 more)

### Community 15 - "Community 15"
Cohesion: 0.1
Nodes (1): test_that_an_agent_can_be_created_with_tags()

### Community 16 - "Community 16"
Cohesion: 0.13
Nodes (19): get_qwen_base_url(), Test that QWEN_BASE_URL works without QWEN_REGION set., Test that missing DASHSCOPE_API_KEY returns error message., Test that verify_environment returns error for invalid QWEN_REGION., Test that get_qwen_base_url returns international URL by default., Test that get_qwen_base_url returns domestic URL when QWEN_REGION is domestic., Test that get_qwen_base_url returns international URL when QWEN_REGION is intern, Test that QWEN_REGION is case insensitive. (+11 more)

### Community 17 - "Community 17"
Cohesion: 0.14
Nodes (1): test_that_a_capability_can_be_created_with_tags()

### Community 19 - "Community 19"
Cohesion: 0.14
Nodes (4): do_generate(), get_embedder(), get_moderation_service(), _infer_dims()

### Community 20 - "Community 20"
Cohesion: 0.23
Nodes (5): _create_auto_model(), _create_tokenizer(), do_embed(), _get_device(), _model_temp_dir()

### Community 21 - "Community 21"
Cohesion: 0.17
Nodes (3): do_generate(), get_embedder(), get_moderation_service()

### Community 22 - "Community 22"
Cohesion: 0.24
Nodes (4): add_domain_glossary(), create_booking_status_journey(), create_flight_booking_journey(), main()

### Community 23 - "Community 23"
Cohesion: 0.2
Nodes (11): SchematicGenerator, StreamingTextGenerator, GuidelineMatcher, GuidelineMatchingResult, BuiltInSection, PromptBuilder, PromptSection, ServiceRegistry (+3 more)

### Community 24 - "Community 24"
Cohesion: 0.27
Nodes (4): add_domain_glossary(), create_lab_results_journey(), create_scheduling_journey(), main()

### Community 26 - "Community 26"
Cohesion: 0.39
Nodes (7): get(), get_agent(), get_context_creation(), get_customer(), get_interaction(), get_session(), get_variable_value()

### Community 27 - "Community 27"
Cohesion: 0.22
Nodes (1): is_preamble_required()

### Community 28 - "Community 28"
Cohesion: 0.28
Nodes (1): AgentModule

### Community 29 - "Community 29"
Cohesion: 0.28
Nodes (1): GlossaryModule

### Community 30 - "Community 30"
Cohesion: 0.28
Nodes (1): CapabilityModule

### Community 31 - "Community 31"
Cohesion: 0.22
Nodes (9): Custom NLP Models, Embedder, Estimating Tokenizer, ModerationService, NLPService, PromptBuilder, SchematicGenerator, Attentive Reasoning Queries (ARQs) (+1 more)

### Community 32 - "Community 32"
Cohesion: 0.29
Nodes (3): do_embed(), _make_unique_text(), test_that_cache_eviction_preserves_entries_with_the_same_text_length()

### Community 33 - "Community 33"
Cohesion: 0.25
Nodes (1): Convert the log level to an integer for comparison.

### Community 35 - "Community 35"
Cohesion: 0.25
Nodes (1): TagModule

### Community 36 - "Community 36"
Cohesion: 0.25
Nodes (2): useWebSocket(), WebSocketComp()

### Community 37 - "Community 37"
Cohesion: 0.29
Nodes (6): Test latch behavior when task is cancelled but latch suppresses it., Test latch behavior when task is cancelled but latch suppresses it., Test latch behavior when task is cancelled but latch suppresses it., test_latch_behavior_with_cancellation_after_suppression(), test_latch_behavior_with_cancellation_before_suppression(), test_latch_behavior_with_no_cancellation()

### Community 38 - "Community 38"
Cohesion: 0.52
Nodes (6): base_test_tool_running_action_detector(), test_that_guideline_with_action_that_not_only_require_running_tools_is_not_detected(), test_that_guideline_with_action_that_only_run_several_tools_is_detected(), test_that_guideline_with_action_that_only_run_tool_is_detected(), test_that_guideline_with_action_that_require_a_tool_but_unrelated_associated_tool_is_not_detected(), test_that_guideline_with_action_that_require_running_tools_and_telling_the_user_something_is_not_detected()

### Community 40 - "Community 40"
Cohesion: 0.43
Nodes (4): get_or_create_variable(), given_a_context_variable_to_specific_customer(), given_a_context_variable_with_freshness_rules(), given_a_context_variable_with_tool()

### Community 44 - "Community 44"
Cohesion: 0.33
Nodes (1): ErrorBoundary

### Community 45 - "Community 45"
Cohesion: 0.5
Nodes (2): load_steps(), Step

### Community 47 - "Community 47"
Cohesion: 0.83
Nodes (3): _stub_embedder(), test_that_deleting_a_capability_removes_its_vector_documents(), test_that_updating_a_capability_replaces_its_vector_documents()

### Community 48 - "Community 48"
Cohesion: 0.83
Nodes (3): check_guideline(), test_that_actions_which_are_customer_dependent_are_classified_correctly(), test_that_actions_which_are_not_customer_dependent_are_classified_correctly()

### Community 51 - "Community 51"
Cohesion: 0.5
Nodes (4): Agent Context Diagram, Prompt Builder Diagram, Context Variable Diagram, Glossary Diagram

### Community 52 - "Community 52"
Cohesion: 0.67
Nodes (2): test_that_continuous_guidelines_mark_as_continuous(), test_that_non_continuous_guidelines_mark_as_non_continuous()

### Community 55 - "Community 55"
Cohesion: 1.0
Nodes (2): selectAgent(), selectCustomer()

### Community 60 - "Community 60"
Cohesion: 1.0
Nodes (2): objToUrlParams(), useFetch()

### Community 62 - "Community 62"
Cohesion: 0.67
Nodes (3): Docker installation, Parlant Installation, pip install

### Community 63 - "Community 63"
Cohesion: 0.67
Nodes (3): Agentic AI, Customer Experience (CX), Parlant Motivation

### Community 64 - "Community 64"
Cohesion: 0.67
Nodes (3): DocumentCollection, DocumentDatabase, ServiceDocumentRegistry

### Community 91 - "Community 91"
Cohesion: 1.0
Nodes (2): SDKTest, Parlant Testing Output

### Community 92 - "Community 92"
Cohesion: 1.0
Nodes (2): Gemini Service Diagram, OpenAI Service Diagram

### Community 93 - "Community 93"
Cohesion: 1.0
Nodes (2): Guideline Match Diagram, Guideline Matcher Diagram

### Community 94 - "Community 94"
Cohesion: 1.0
Nodes (2): Inference Data Diagram, Inference Result Diagram

### Community 95 - "Community 95"
Cohesion: 1.0
Nodes (2): Test_that_an_agent_can_be_created, nlp_test

### Community 96 - "Community 96"
Cohesion: 1.0
Nodes (2): Engine Extensions, Engine Hooks

### Community 97 - "Community 97"
Cohesion: 1.0
Nodes (2): Guideline Priority, Journey Transition

### Community 104 - "Community 104"
Cohesion: 1.0
Nodes (1): Return the most recent health snapshot.

### Community 106 - "Community 106"
Cohesion: 1.0
Nodes (1): Determines whether to use the embedding cache.

### Community 107 - "Community 107"
Cohesion: 1.0
Nodes (1): Gets the batch size for guideline matching.

### Community 108 - "Community 108"
Cohesion: 1.0
Nodes (1): Gets the retry temperatures (and number of generation attempts) for a guideline

### Community 109 - "Community 109"
Cohesion: 1.0
Nodes (1): Gets the retry temperatures (and number of generation attempts) for a response a

### Community 110 - "Community 110"
Cohesion: 1.0
Nodes (1): Gets the retry temperatures (and number of generation attempts) for a tool calli

### Community 111 - "Community 111"
Cohesion: 1.0
Nodes (1): Gets the retry temperatures (and number of generation attempts) for guideline pr

### Community 114 - "Community 114"
Cohesion: 1.0
Nodes (1): Render a list of dictionaries as a rich table.          If *header_order* is pro

### Community 141 - "Community 141"
Cohesion: 1.0
Nodes (1): Engine Hooks

### Community 142 - "Community 142"
Cohesion: 1.0
Nodes (1): Dependency Injection Container

### Community 143 - "Community 143"
Cohesion: 1.0
Nodes (1): Lakera Guard

### Community 144 - "Community 144"
Cohesion: 1.0
Nodes (1): Developer Certificate of Origin

### Community 145 - "Community 145"
Cohesion: 1.0
Nodes (1): ParlantClient

### Community 146 - "Community 146"
Cohesion: 1.0
Nodes (1): Graph Visualization

### Community 147 - "Community 147"
Cohesion: 1.0
Nodes (1): GitHub Action Disk Cleanup Script

### Community 148 - "Community 148"
Cohesion: 1.0
Nodes (1): Fern Documentation Config

### Community 149 - "Community 149"
Cohesion: 1.0
Nodes (1): Chat Lifecycle Diagram

### Community 150 - "Community 150"
Cohesion: 1.0
Nodes (1): Contextual Correlator Diagram

### Community 151 - "Community 151"
Cohesion: 1.0
Nodes (1): Event Emitter Diagram

### Community 152 - "Community 152"
Cohesion: 1.0
Nodes (1): Plugin Diagram

### Community 153 - "Community 153"
Cohesion: 1.0
Nodes (1): Previously Applied Actionable BAT Match Diagram

### Community 154 - "Community 154"
Cohesion: 1.0
Nodes (1): Tool Caller Diagram

### Community 155 - "Community 155"
Cohesion: 1.0
Nodes (1): Tool Insight Diagram

### Community 156 - "Community 156"
Cohesion: 1.0
Nodes (1): ToolCall

### Community 157 - "Community 157"
Cohesion: 1.0
Nodes (1): Bug Report Template

### Community 158 - "Community 158"
Cohesion: 1.0
Nodes (1): Feature Request Template

### Community 159 - "Community 159"
Cohesion: 1.0
Nodes (1): Contributing to Parlant

### Community 160 - "Community 160"
Cohesion: 1.0
Nodes (1): Dependency Injection

### Community 161 - "Community 161"
Cohesion: 1.0
Nodes (1): Session Label Propagation

### Community 162 - "Community 162"
Cohesion: 1.0
Nodes (1): Variable Precedence

### Community 163 - "Community 163"
Cohesion: 1.0
Nodes (1): Tool

## Knowledge Gaps
- **118 isolated node(s):** `Condition guidelines (tagged with journey tag but no journey_node metadata)`, `G1 depend_on_any(G2, G3) AND depend_on_any(G4, G5).     G2 matched (group A met)`, `Wait for the server port to be ready to accept connections.`, `Event loop health status following incident.io conventions.`, `Snapshot of event loop health.` (+113 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Community 15`** (20 nodes): `test_that_agent_composition_mode_can_be_set_and_updated()`, `test_that_an_agent_can_be_created_with_custom_id()`, `test_that_an_agent_can_be_created_with_default_composition_mode()`, `test_that_an_agent_can_be_created_with_description()`, `test_that_an_agent_can_be_created_with_max_engine_iterations()`, `test_that_an_agent_can_be_created_with_specific_composition_mode()`, `test_that_an_agent_can_be_created_with_tags()`, `test_that_an_agent_can_be_created_without_description()`, `test_that_an_agent_can_be_created_without_max_engine_iterations()`, `test_that_an_agent_can_be_deleted()`, `test_that_an_agent_can_be_listed()`, `test_that_an_agent_can_be_read()`, `test_that_an_agent_can_be_updated()`, `test_that_an_agent_cannot_be_created_with_a_nonexistent_tag()`, `test_that_creating_agent_with_duplicate_custom_id_fails()`, `test_that_multiple_agents_can_be_created_with_different_custom_ids()`, `test_that_tags_can_be_added_and_removed_in_same_request()`, `test_that_tags_can_be_added_to_an_agent()`, `test_that_tags_can_be_removed_from_an_agent()`, `test_agents.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 17`** (14 nodes): `test_that_a_capability_can_be_created()`, `test_that_a_capability_can_be_created_with_tags()`, `test_that_a_capability_can_be_deleted()`, `test_that_a_capability_can_be_read()`, `test_that_a_capability_can_be_updated()`, `test_that_agent_tag_can_be_added_to_a_capability()`, `test_that_agent_tag_can_be_removed_from_a_capability()`, `test_that_capabilities_can_be_filtered_by_tag()`, `test_that_capabilities_can_be_listed()`, `test_that_journey_tags_can_be_added_to_a_capability()`, `test_that_journey_tags_can_be_removed_from_a_capability()`, `test_that_tags_can_be_added_to_a_capability()`, `test_that_tags_can_be_removed_from_a_capability()`, `test_capabilities.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 27`** (9 nodes): `._calculate_previous_customer_wait_times()`, `._last_agent_message_is_preamble()`, `get_extended_processing_indicator_delay()`, `get_follow_up_delay()`, `get_preamble_delay()`, `get_processing_indicator_delay()`, `is_message_splitting_required()`, `is_preamble_required()`, `perceived_performance_policy.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 28`** (9 nodes): `AgentModule`, `.create()`, `.delete()`, `._ensure_tag()`, `.find()`, `.__init__()`, `.read()`, `.update()`, `agents.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 29`** (9 nodes): `GlossaryModule`, `.create()`, `.delete()`, `._ensure_tag()`, `.find()`, `.__init__()`, `.read()`, `.update()`, `glossary.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 30`** (9 nodes): `CapabilityModule`, `.create()`, `.delete()`, `._ensure_tag()`, `.find()`, `.__init__()`, `.read()`, `.update()`, `capabilities.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 33`** (8 nodes): `.__eq__()`, `.__ge__()`, `.__gt__()`, `.__le__()`, `.__lt__()`, `.__ne__()`, `.to_int()`, `Convert the log level to an integer for comparison.`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 35`** (8 nodes): `TagModule`, `.create()`, `.delete()`, `.find()`, `.__init__()`, `.read()`, `.update()`, `tags.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 36`** (8 nodes): `useWebSocket()`, `App()`, `WebSocketComp()`, `App.tsx`, `sonner.tsx`, `useWebSocket.ts`, `main.tsx`, `Toaster()`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 44`** (6 nodes): `ErrorBoundary`, `.componentDidCatch()`, `.constructor()`, `.getDerivedStateFromError()`, `.render()`, `error-boundary.tsx`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 45`** (5 nodes): `load_steps()`, `Step`, `.__init__()`, `.install()`, `utils.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 52`** (3 nodes): `test_that_continuous_guidelines_mark_as_continuous()`, `test_that_non_continuous_guidelines_mark_as_non_continuous()`, `test_continuous_guideline_proposer.py`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 55`** (3 nodes): `selectAgent()`, `selectCustomer()`, `agent-list.tsx`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 60`** (3 nodes): `objToUrlParams()`, `useFetch()`, `useFetch.tsx`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 91`** (2 nodes): `SDKTest`, `Parlant Testing Output`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 92`** (2 nodes): `Gemini Service Diagram`, `OpenAI Service Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 93`** (2 nodes): `Guideline Match Diagram`, `Guideline Matcher Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 94`** (2 nodes): `Inference Data Diagram`, `Inference Result Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 95`** (2 nodes): `Test_that_an_agent_can_be_created`, `nlp_test`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 96`** (2 nodes): `Engine Extensions`, `Engine Hooks`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 97`** (2 nodes): `Guideline Priority`, `Journey Transition`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 104`** (1 nodes): `Return the most recent health snapshot.`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 106`** (1 nodes): `Determines whether to use the embedding cache.`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 107`** (1 nodes): `Gets the batch size for guideline matching.`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 108`** (1 nodes): `Gets the retry temperatures (and number of generation attempts) for a guideline`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 109`** (1 nodes): `Gets the retry temperatures (and number of generation attempts) for a response a`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 110`** (1 nodes): `Gets the retry temperatures (and number of generation attempts) for a tool calli`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 111`** (1 nodes): `Gets the retry temperatures (and number of generation attempts) for guideline pr`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 114`** (1 nodes): `Render a list of dictionaries as a rich table.          If *header_order* is pro`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 141`** (1 nodes): `Engine Hooks`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 142`** (1 nodes): `Dependency Injection Container`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 143`** (1 nodes): `Lakera Guard`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 144`** (1 nodes): `Developer Certificate of Origin`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 145`** (1 nodes): `ParlantClient`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 146`** (1 nodes): `Graph Visualization`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 147`** (1 nodes): `GitHub Action Disk Cleanup Script`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 148`** (1 nodes): `Fern Documentation Config`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 149`** (1 nodes): `Chat Lifecycle Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 150`** (1 nodes): `Contextual Correlator Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 151`** (1 nodes): `Event Emitter Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 152`** (1 nodes): `Plugin Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 153`** (1 nodes): `Previously Applied Actionable BAT Match Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 154`** (1 nodes): `Tool Caller Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 155`** (1 nodes): `Tool Insight Diagram`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 156`** (1 nodes): `ToolCall`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 157`** (1 nodes): `Bug Report Template`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 158`** (1 nodes): `Feature Request Template`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 159`** (1 nodes): `Contributing to Parlant`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 160`** (1 nodes): `Dependency Injection`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 161`** (1 nodes): `Session Label Propagation`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 162`** (1 nodes): `Variable Precedence`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 163`** (1 nodes): `Tool`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Logger` connect `Canned Responses & Data Models` to `Alpha Engine & Guideline Matching`, `DTO Mappings & Configuration`, `Prompt Engineering & Drafting`, `Policies & Perceived Performance`, `Response Generation & No-Match Handling`, `System Health & Monitoring`, `Community 35`, `Community 28`, `Community 29`, `Community 30`?**
  _High betweenness centrality (0.115) - this node is a cross-community bridge._
- **Why does `ToolId` connect `Alpha Engine & Guideline Matching` to `Canned Responses & Data Models`, `DTO Mappings & Configuration`, `Prompt Engineering & Drafting`, `Policies & Perceived Performance`, `Response Generation & No-Match Handling`, `Community 38`, `Session & Entity Management`, `Community 40`, `Journey & Guideline Integration`?**
  _High betweenness centrality (0.046) - this node is a cross-community bridge._
- **Why does `Tracer` connect `Canned Responses & Data Models` to `Alpha Engine & Guideline Matching`, `DTO Mappings & Configuration`, `Prompt Engineering & Drafting`, `Policies & Perceived Performance`, `Response Generation & No-Match Handling`, `System Health & Monitoring`, `Community 33`?**
  _High betweenness centrality (0.045) - this node is a cross-community bridge._
- **Are the 1120 inferred relationships involving `Logger` (e.g. with `NLPTestSchema` and `SyncAwaiter`) actually correct?**
  _`Logger` has 1120 INFERRED edges - model-reasoned connections that need verification._
- **Are the 875 inferred relationships involving `Tracer` (e.g. with `CacheOptions` and `NoCachedGenerations`) actually correct?**
  _`Tracer` has 875 INFERRED edges - model-reasoned connections that need verification._
- **Are the 824 inferred relationships involving `Meter` (e.g. with `CacheOptions` and `NoCachedGenerations`) actually correct?**
  _`Meter` has 824 INFERRED edges - model-reasoned connections that need verification._
- **Are the 720 inferred relationships involving `PromptBuilder` (e.g. with `NLPTestSchema` and `SyncAwaiter`) actually correct?**
  _`PromptBuilder` has 720 INFERRED edges - model-reasoned connections that need verification._