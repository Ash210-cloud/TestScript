{% extends "base.html" %}

{% block title %}
Dashboard | Sales & Inventory AI
{% endblock %}

{% block content %}

<style>

/* ============================================================
   SALES & INVENTORY AI
   MODERN DASHBOARD OVERRIDES
   ============================================================ */

.dashboard-page {
    width: 100%;
    max-width: 1600px;
    margin: 0 auto;
    padding: 32px;
}


/* ============================================================
   HEADER
   ============================================================ */

.dashboard-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 24px;
    margin-bottom: 28px;
}

.dashboard-eyebrow {
    margin: 0 0 8px 0;
    color: #15803d;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 1.8px;
    text-transform: uppercase;
}

.dashboard-header h1 {
    margin: 0;
    color: #111827;
    font-size: 36px;
    line-height: 1.15;
    font-weight: 800;
    letter-spacing: -0.8px;
}

.dashboard-subtitle {
    margin: 10px 0 0 0;
    color: #6b7280;
    font-size: 14px;
    line-height: 1.6;
}


/* ============================================================
   STATUS
   ============================================================ */

.dashboard-status {
    display: inline-flex;
    align-items: center;
    gap: 9px;
    padding: 10px 15px;
    background: #ffffff;
    border: 1px solid #dcfce7;
    border-radius: 999px;
    color: #166534;
    font-size: 12px;
    font-weight: 700;
    white-space: nowrap;
    box-shadow: 0 4px 15px rgba(15, 23, 42, 0.04);
}

.status-dot {
    width: 8px;
    height: 8px;
    background: #22c55e;
    border-radius: 50%;
    box-shadow: 0 0 0 4px rgba(34, 197, 94, 0.12);
}


/* ============================================================
   GENERAL CARD
   ============================================================ */

.dashboard-card {
    min-width: 0;
    padding: 24px;
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 18px;
    box-shadow:
        0 6px 20px rgba(15, 23, 42, 0.04);
}


/* ============================================================
   CARD HEADER
   ============================================================ */

.card-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 16px;
    margin-bottom: 20px;
}

.card-eyebrow {
    margin: 0 0 6px 0;
    color: #15803d;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 1.5px;
    text-transform: uppercase;
}

.card-header h2 {
    margin: 0;
    color: #111827;
    font-size: 18px;
    line-height: 1.3;
    font-weight: 800;
}

.card-description {
    margin: 7px 0 0 0;
    color: #6b7280;
    font-size: 13px;
    line-height: 1.5;
}


/* ============================================================
   DATASET UPLOAD CARD
   ============================================================ */

.dataset-upload-card {
    margin-bottom: 22px;
    padding: 0;
    overflow: hidden;
}

.dataset-upload-card > .card-header {
    margin: 0;
    padding: 24px 26px 20px;
    border-bottom: 1px solid #eef2f0;
}


/* ============================================================
   DROP ZONE
   ============================================================ */

.dataset-drop-zone,
#datasetDropZone {
    position: relative;

    width: 100%;
    min-height: 190px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    padding: 30px 24px;

    background:
        linear-gradient(
            135deg,
            #fbfefc 0%,
            #f5faf7 100%
        ) !important;

    border: 2px dashed #b7d8c2 !important;
    border-radius: 14px !important;

    cursor: pointer;
    text-align: center;

    transition:
        background 0.2s ease,
        border-color 0.2s ease,
        box-shadow 0.2s ease,
        transform 0.2s ease;

    overflow: hidden;

    margin: 20px 26px 24px;
    width: calc(100% - 52px);
}


/* ============================================================
   DROP ZONE HOVER
   ============================================================ */

.dataset-drop-zone:hover,
#datasetDropZone:hover {
    background:
        linear-gradient(
            135deg,
            #f4fcf7 0%,
            #ecfdf5 100%
        ) !important;

    border-color: #4ade80 !important;

    box-shadow:
        0 8px 25px rgba(22, 163, 74, 0.07);

    transform: translateY(-1px);
}


/* ============================================================
   DRAG OVER
   ============================================================ */

.dataset-drop-zone.drag-over,
#datasetDropZone.drag-over {
    background:
        linear-gradient(
            135deg,
            #ecfdf5 0%,
            #dcfce7 100%
        ) !important;

    border-color: #16a34a !important;

    box-shadow:
        0 0 0 4px rgba(22, 163, 74, 0.08),
        0 12px 30px rgba(22, 163, 74, 0.08);

    transform: scale(1.002);
}


/* ============================================================
   UPLOAD ICON
   ============================================================ */

.dataset-upload-icon,
#datasetDropZone .dataset-upload-icon {
    width: 58px;
    height: 58px;

    display: flex;
    align-items: center;
    justify-content: center;

    margin: 0 0 14px;

    background: #dcfce7;

    border: 1px solid #bbf7d0;

    border-radius: 14px;

    color: #15803d;

    font-size: 27px;

    box-shadow:
        0 6px 15px rgba(22, 163, 74, 0.08);

    flex-shrink: 0;
}


/* ============================================================
   UPLOAD TITLE
   ============================================================ */

.dataset-upload-title,
#datasetDropZone .dataset-upload-title {
    margin: 0;

    color: #111827;

    font-size: 17px;

    line-height: 1.3;

    font-weight: 800;
}


/* ============================================================
   BROWSE TEXT
   ============================================================ */

.dataset-upload-description,
#datasetDropZone .dataset-upload-description {
    margin-top: 6px;

    color: #15803d;

    font-size: 13px;

    font-weight: 700;
}


/* ============================================================
   FILE SUPPORT
   ============================================================ */

.dataset-upload-supported,
#datasetDropZone .dataset-upload-supported {
    margin-top: 6px;

    color: #9ca3af;

    font-size: 12px;
}


/* ============================================================
   HIDDEN FILE INPUT
   ============================================================ */

#datasetFileInput {
    display: none;
}


/* ============================================================
   UPLOAD STATUS
   ============================================================ */

.dataset-upload-status {
    display: flex;

    align-items: center;

    min-height: 54px;

    margin: 0 26px 24px;

    padding: 12px 16px;

    background: #f8faf9;

    border: 1px solid #dce8df;

    border-radius: 12px;

    color: #374151;

    font-size: 13px;

    line-height: 1.5;
}

.dataset-upload-status.upload-success,
.dataset-upload-status.success {
    background: #f0fdf4;
    border-color: #bbf7d0;
    color: #166534;
}

.dataset-upload-status.upload-analyzing,
.dataset-upload-status.analyzing {
    background: #eff6ff;
    border-color: #bfdbfe;
    color: #1d4ed8;
}

.dataset-upload-status.upload-error,
.dataset-upload-status.error {
    background: #fef2f2;
    border-color: #fecaca;
    color: #b91c1c;
}


/* ============================================================
   KPI GRID
   ============================================================ */

.kpi-grid {
    display: grid;

    grid-template-columns:
        repeat(4, minmax(0, 1fr));

    gap: 16px;

    margin-bottom: 22px;
}


/* ============================================================
   KPI CARD
   ============================================================ */

.kpi-card {
    position: relative;
    overflow: hidden;

    min-width: 0;

    padding: 20px;

    background: #ffffff;

    border: 1px solid #e5e7eb;

    border-radius: 16px;

    box-shadow:
        0 6px 20px rgba(15, 23, 42, 0.04);

    transition:
        transform 0.2s ease,
        box-shadow 0.2s ease,
        border-color 0.2s ease;
}

.kpi-card::before {
    content: "";

    position: absolute;

    top: 0;
    left: 0;

    width: 100%;
    height: 3px;

    background: #16a34a;
}

.kpi-card::after {
    content: "";

    position: absolute;

    width: 100px;
    height: 100px;

    right: -38px;
    bottom: -50px;

    background: #ecfdf5;

    border-radius: 50%;

    pointer-events: none;
}

.kpi-card:hover {
    transform: translateY(-2px);

    border-color: #bbf7d0;

    box-shadow:
        0 12px 30px rgba(15, 23, 42, 0.07);
}


/* ============================================================
   KPI HEADER
   ============================================================ */

.kpi-card-header {
    position: relative;
    z-index: 1;

    display: flex;

    align-items: center;

    justify-content: space-between;

    gap: 12px;
}

.kpi-label {
    color: #6b7280;

    font-size: 12px;

    font-weight: 700;
}

.kpi-icon {
    position: relative;
    z-index: 1;

    display: flex;

    align-items: center;

    justify-content: center;

    width: 32px;
    height: 32px;

    background: #ecfdf5;

    border: 1px solid #d1fae5;

    border-radius: 9px;

    color: #16a34a;

    font-size: 15px;

    font-weight: 800;
}


/* ============================================================
   KPI VALUE
   ============================================================ */

.kpi-value {
    position: relative;
    z-index: 1;

    margin-top: 17px;

    color: #111827;

    font-size: 28px;

    line-height: 1;

    font-weight: 800;

    letter-spacing: -0.7px;
}

.kpi-description {
    position: relative;
    z-index: 1;

    margin-top: 9px;

    color: #9ca3af;

    font-size: 11px;
}


/* ============================================================
   MAIN DASHBOARD GRID
   ============================================================ */

.dashboard-grid {
    display: grid;

    grid-template-columns:
        repeat(2, minmax(0, 1fr));

    gap: 16px;

    margin-bottom: 22px;
}


/* ============================================================
   SALES OVERVIEW
   ============================================================ */

.sales-overview {
    grid-column: span 2;
}


/* ============================================================
   CHART
   ============================================================ */

.chart-placeholder {
    min-height: 280px;

    display: flex;

    align-items: center;

    justify-content: center;

    background:
        linear-gradient(
            135deg,
            #f8faf9,
            #f0fdf4
        );

    border: 1px dashed #bbf7d0;

    border-radius: 14px;
}

.chart-placeholder-content {
    text-align: center;
}

.chart-placeholder-icon {
    display: inline-flex;

    align-items: center;

    justify-content: center;

    width: 52px;
    height: 52px;

    margin-bottom: 13px;

    background: #dcfce7;

    border-radius: 14px;

    color: #16a34a;

    font-size: 23px;

    font-weight: 800;
}

.chart-placeholder-content h3 {
    margin: 0;

    color: #111827;

    font-size: 16px;

    font-weight: 800;
}

.chart-placeholder-content p {
    margin: 7px 0 0;

    color: #9ca3af;

    font-size: 12px;
}


/* ============================================================
   CARD ACTION
   ============================================================ */

.card-action {
    padding: 8px 13px;

    background: #f0fdf4;

    border: 1px solid #bbf7d0;

    border-radius: 8px;

    color: #15803d;

    font-size: 11px;

    font-weight: 700;

    cursor: pointer;

    transition:
        background 0.2s ease,
        color 0.2s ease;
}

.card-action:hover {
    background: #16a34a;
    color: #ffffff;
}


/* ============================================================
   INSIGHT CARDS
   ============================================================ */

.insight-content {
    min-height: 145px;

    display: flex;

    flex-direction: column;

    justify-content: center;

    padding: 2px 0;
}

.insight-label {
    margin-bottom: 8px;

    color: #9ca3af;

    font-size: 9px;

    font-weight: 800;

    letter-spacing: 1.4px;
}

.insight-value {
    color: #111827;

    font-size: 20px;

    line-height: 1.3;

    font-weight: 800;

    word-break: break-word;
}

.insight-metric {
    margin-top: 10px;

    color: #16a34a;

    font-size: 23px;

    line-height: 1;

    font-weight: 800;
}

.insight-description {
    margin-top: 6px;

    color: #9ca3af;

    font-size: 11px;
}


/* ============================================================
   AI QUERY
   ============================================================ */

.ai-query-card {
    margin-bottom: 30px;
}

.ai-query-form {
    display: flex;

    align-items: stretch;

    gap: 10px;
}

.ai-query-input {
    flex: 1;

    min-width: 0;

    height: 48px;

    padding: 0 15px;

    background: #f9fafb;

    border: 1px solid #d1d5db;

    border-radius: 10px;

    outline: none;

    color: #111827;

    font-family: inherit;

    font-size: 13px;

    transition:
        border-color 0.2s ease,
        box-shadow 0.2s ease,
        background 0.2s ease;
}

.ai-query-input::placeholder {
    color: #9ca3af;
}

.ai-query-input:focus {
    background: #ffffff;

    border-color: #16a34a;

    box-shadow:
        0 0 0 3px rgba(22, 163, 74, 0.10);
}


/* ============================================================
   AI BUTTON
   ============================================================ */

.ai-query-button {
    min-width: 105px;

    height: 48px;

    padding: 0 18px;

    background: #111827;

    border: 1px solid #111827;

    border-radius: 10px;

    color: #ffffff;

    font-family: inherit;

    font-size: 13px;

    font-weight: 800;

    cursor: pointer;

    transition:
        background 0.2s ease,
        transform 0.2s ease;
}

.ai-query-button:hover {
    background: #16a34a;

    border-color: #16a34a;

    transform: translateY(-1px);
}

.ai-query-button:disabled {
    opacity: 0.65;

    cursor: not-allowed;

    transform: none;
}


/* ============================================================
   AI RESPONSE
   ============================================================ */

.ai-response {
    margin-top: 16px;

    padding: 17px;

    background: #f0fdf4;

    border: 1px solid #bbf7d0;

    border-left: 4px solid #16a34a;

    border-radius: 12px;
}

.ai-response-header {
    margin-bottom: 7px;
}

.ai-response-label {
    color: #15803d;

    font-size: 9px;

    font-weight: 800;

    letter-spacing: 1.4px;
}

.ai-response-text {
    color: #1f2937;

    font-size: 13px;

    line-height: 1.7;

    white-space: pre-line;
}


/* ============================================================
   AI QUESTION SELECTOR
   ============================================================ */

.ai-question-selector {
    display: flex;

    align-items: stretch;

    gap: 10px;

    width: 100%;
}

.ai-question-selector-display {
    flex: 1;

    min-width: 0;

    height: 48px;

    display: flex;

    align-items: center;

    padding: 0 15px;

    background: #f9fafb;

    border: 1px solid #d1d5db;

    border-radius: 10px;

    color: #9ca3af;

    font-size: 13px;

    overflow: hidden;

    white-space: nowrap;

    text-overflow: ellipsis;
}

.ai-question-selector-display.has-question {
    color: #111827;
}

.ai-question-selector-button {
    height: 48px;

    min-width: 125px;

    padding: 0 18px;

    background: #111827;

    border: 1px solid #111827;

    border-radius: 10px;

    color: #ffffff;

    font-family: inherit;

    font-size: 13px;

    font-weight: 800;

    cursor: pointer;

    transition:
        background 0.2s ease,
        transform 0.2s ease;
}

.ai-question-selector-button:hover {
    background: #16a34a;

    border-color: #16a34a;

    transform: translateY(-1px);
}


/* ============================================================
   RESET BUTTON
   ============================================================ */

.ai-question-reset-button {
    height: 48px;

    min-width: 90px;

    padding: 0 18px;

    background: #ffffff;

    border: 1px solid #d1d5db;

    border-radius: 10px;

    color: #6b7280;

    font-family: inherit;

    font-size: 13px;

    font-weight: 800;

    cursor: pointer;

    transition:
        background 0.2s ease,
        color 0.2s ease,
        border-color 0.2s ease,
        transform 0.2s ease;
}

.ai-question-reset-button:hover {
    background: #fef2f2;

    border-color: #fecaca;

    color: #dc2626;

    transform: translateY(-1px);
}


/* ============================================================
   QUESTION MODAL OVERLAY
   ============================================================ */

.ai-question-modal {
    position: fixed;

    inset: 0;

    z-index: 9999;

    display: none;

    align-items: center;

    justify-content: center;

    padding: 24px;

    background: rgba(15, 23, 42, 0.48);

    backdrop-filter: blur(5px);

    -webkit-backdrop-filter: blur(5px);
}

.ai-question-modal.active {
    display: flex;

    animation: aiModalFadeIn 0.18s ease;
}


/* ============================================================
   MODAL
   ============================================================ */

.ai-question-modal-content {
    width: 100%;

    max-width: 720px;

    max-height: min(720px, 90vh);

    display: flex;

    flex-direction: column;

    overflow: hidden;

    background: #ffffff;

    border: 1px solid #e5e7eb;

    border-radius: 20px;

    box-shadow:
        0 25px 70px rgba(15, 23, 42, 0.20);
}


/* ============================================================
   MODAL HEADER
   ============================================================ */

.ai-question-modal-header {
    display: flex;

    align-items: flex-start;

    justify-content: space-between;

    gap: 16px;

    padding: 24px 24px 18px;

    border-bottom: 1px solid #eef2f0;
}

.ai-question-modal-header-left {
    min-width: 0;
}

.ai-question-modal-eyebrow {
    margin: 0 0 6px;

    color: #15803d;

    font-size: 9px;

    font-weight: 800;

    letter-spacing: 1.5px;

    text-transform: uppercase;
}

.ai-question-modal-title {
    margin: 0;

    color: #111827;

    font-size: 21px;

    line-height: 1.25;

    font-weight: 800;
}

.ai-question-modal-description {
    margin: 6px 0 0;

    color: #6b7280;

    font-size: 12px;

    line-height: 1.5;
}


/* ============================================================
   MODAL CLOSE
   ============================================================ */

.ai-question-modal-close {
    flex-shrink: 0;

    width: 36px;
    height: 36px;

    display: flex;

    align-items: center;

    justify-content: center;

    background: #f9fafb;

    border: 1px solid #e5e7eb;

    border-radius: 10px;

    color: #6b7280;

    font-size: 20px;

    line-height: 1;

    cursor: pointer;

    transition:
        background 0.2s ease,
        color 0.2s ease,
        border-color 0.2s ease;
}

.ai-question-modal-close:hover {
    background: #fef2f2;

    border-color: #fecaca;

    color: #dc2626;
}


/* ============================================================
   QUESTION SEARCH
   ============================================================ */

.ai-question-search-wrapper {
    position: relative;

    padding: 18px 24px 14px;

    background: #ffffff;
}

.ai-question-search-icon {
    position: absolute;

    left: 39px;

    top: 50%;

    transform: translateY(-50%);

    color: #9ca3af;

    font-size: 16px;

    pointer-events: none;
}

.ai-question-search {
    width: 100%;

    height: 46px;

    padding: 0 15px 0 42px;

    background: #f9fafb;

    border: 1px solid #d1d5db;

    border-radius: 11px;

    outline: none;

    color: #111827;

    font-family: inherit;

    font-size: 13px;

    transition:
        background 0.2s ease,
        border-color 0.2s ease,
        box-shadow 0.2s ease;
}

.ai-question-search::placeholder {
    color: #9ca3af;
}

.ai-question-search:focus {
    background: #ffffff;

    border-color: #16a34a;

    box-shadow:
        0 0 0 3px rgba(22, 163, 74, 0.10);
}


/* ============================================================
   QUESTION LIST
   ============================================================ */

.ai-question-list {
    flex: 1;

    min-height: 0;

    overflow-y: auto;

    padding: 4px 24px 24px;
}

.ai-question-category {
    margin-top: 14px;
}

.ai-question-category:first-child {
    margin-top: 4px;
}

.ai-question-category-title {
    margin: 0 0 8px;

    color: #9ca3af;

    font-size: 9px;

    font-weight: 800;

    letter-spacing: 1.3px;

    text-transform: uppercase;
}


/* ============================================================
   QUESTION ITEM
   ============================================================ */

.ai-question-item {
    width: 100%;

    display: flex;

    align-items: center;

    justify-content: space-between;

    gap: 14px;

    padding: 13px 14px;

    margin-bottom: 6px;

    background: #ffffff;

    border: 1px solid #e5e7eb;

    border-radius: 11px;

    color: #1f2937;

    font-family: inherit;

    font-size: 13px;

    line-height: 1.45;

    text-align: left;

    cursor: pointer;

    transition:
        background 0.18s ease,
        border-color 0.18s ease,
        transform 0.18s ease,
        box-shadow 0.18s ease;
}

.ai-question-item:hover {
    background: #f0fdf4;

    border-color: #bbf7d0;

    transform: translateX(2px);

    box-shadow:
        0 4px 12px rgba(22, 163, 74, 0.06);
}

.ai-question-item-text {
    min-width: 0;
}

.ai-question-item-arrow {
    flex-shrink: 0;

    color: #9ca3af;

    font-size: 15px;

    transition:
        color 0.18s ease,
        transform 0.18s ease;
}

.ai-question-item:hover .ai-question-item-arrow {
    color: #16a34a;

    transform: translateX(2px);
}


/* ============================================================
   EMPTY SEARCH
   ============================================================ */

.ai-question-empty {
    display: none;

    padding: 45px 20px;

    text-align: center;
}

.ai-question-empty-icon {
    width: 46px;
    height: 46px;

    display: inline-flex;

    align-items: center;

    justify-content: center;

    margin-bottom: 12px;

    background: #f3f4f6;

    border-radius: 12px;

    color: #9ca3af;

    font-size: 20px;
}

.ai-question-empty h3 {
    margin: 0;

    color: #374151;

    font-size: 14px;

    font-weight: 800;
}

.ai-question-empty p {
    margin: 6px 0 0;

    color: #9ca3af;

    font-size: 12px;
}


/* ============================================================
   MODAL FOOTER
   ============================================================ */

.ai-question-modal-footer {
    display: flex;

    align-items: center;

    justify-content: space-between;

    gap: 12px;

    padding: 14px 24px;

    background: #fafafa;

    border-top: 1px solid #eef2f0;
}

.ai-question-count {
    color: #9ca3af;

    font-size: 11px;

    font-weight: 600;
}

.ai-question-cancel {
    padding: 8px 14px;

    background: #ffffff;

    border: 1px solid #d1d5db;

    border-radius: 8px;

    color: #6b7280;

    font-family: inherit;

    font-size: 11px;

    font-weight: 700;

    cursor: pointer;

    transition:
        background 0.18s ease,
        color 0.18s ease,
        border-color 0.18s ease;
}

.ai-question-cancel:hover {
    background: #f3f4f6;

    color: #374151;

    border-color: #9ca3af;
}


/* ============================================================
   MODAL ANIMATION
   ============================================================ */

@keyframes aiModalFadeIn {

    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }

}

@keyframes aiModalScaleIn {

    from {
        transform: translateY(8px) scale(0.985);
    }

    to {
        transform: translateY(0) scale(1);
    }

}

.ai-question-modal.active
.ai-question-modal-content {
    animation:
        aiModalScaleIn 0.2s ease;
}


/* ============================================================
   LOADING
   ============================================================ */

.dashboard-loading {
    display: inline-block;

    width: 24px;
    height: 24px;

    border: 3px solid #e5e7eb;

    border-top-color: #16a34a;

    border-radius: 50%;

    animation:
        dashboardLoadingSpin 0.8s linear infinite;
}

@keyframes dashboardLoadingSpin {

    from {
        transform: rotate(0deg);
    }

    to {
        transform: rotate(360deg);
    }

}


/* ============================================================
   RESPONSIVE
   ============================================================ */

@media (max-width: 1200px) {

    .kpi-grid {
        grid-template-columns:
            repeat(2, minmax(0, 1fr));
    }

}


@media (max-width: 900px) {

    .dashboard-page {
        padding: 24px;
    }

    .dashboard-header {
        flex-direction: column;
    }

    .dashboard-grid {
        grid-template-columns: 1fr;
    }

    .sales-overview {
        grid-column: span 1;
    }

}


@media (max-width: 640px) {

    .dashboard-page {
        padding: 16px;
    }

    .dashboard-header {
        margin-bottom: 22px;
    }

    .dashboard-header h1 {
        font-size: 28px;
    }

    .dashboard-subtitle {
        font-size: 13px;
    }

    .dashboard-status {
        width: 100%;
        justify-content: center;
    }

    .kpi-grid {
        grid-template-columns: 1fr;
        gap: 12px;
    }

    .dashboard-grid {
        gap: 12px;
    }

    .dashboard-card {
        padding: 18px;
        border-radius: 14px;
    }

    .dataset-upload-card {
        padding: 0;
    }

    .dataset-upload-card > .card-header {
        padding: 20px 18px 16px;
    }

    .dataset-drop-zone,
    #datasetDropZone {
        min-height: 175px;

        margin: 16px 18px 18px;

        width: calc(100% - 36px);

        padding: 24px 16px;
    }

    .dataset-upload-status {
        margin-left: 18px;
        margin-right: 18px;
    }

    .card-header {
        flex-direction: column;
        gap: 12px;
    }

    .card-action {
        align-self: flex-start;
    }

    .chart-placeholder {
        min-height: 220px;
    }

    .ai-question-selector {
        flex-direction: column;
    }

    .ai-question-selector-button {
        width: 100%;
    }

    .ai-question-reset-button {
        width: 100%;
    }

    .ai-question-modal {
        padding: 12px;
    }

    .ai-question-modal-content {
        max-height: 94vh;

        border-radius: 16px;
    }

    .ai-question-modal-header {
        padding: 20px 18px 16px;
    }

    .ai-question-search-wrapper {
        padding: 16px 18px 12px;
    }

    .ai-question-search-icon {
        left: 33px;
    }

    .ai-question-list {
        padding-left: 18px;
        padding-right: 18px;
    }

    .ai-question-modal-footer {
        padding-left: 18px;
        padding-right: 18px;
    }

}


/* ============================================================
   BODY MODAL LOCK
   ============================================================ */

body.ai-question-modal-open {
    overflow: hidden;
}

</style>


<div class="dashboard-page">

    <!-- ================================================== -->
    <!-- DASHBOARD HEADER -->
    <!-- ================================================== -->

    <section class="dashboard-header">

        <div>

            <p class="dashboard-eyebrow">
                SALES & INVENTORY AI
            </p>

            <h1>
                Sales Dashboard
            </h1>

            <p class="dashboard-subtitle">
                Monitor sales performance, products, dealers,
                regions and business trends.
            </p>

        </div>


        <div class="dashboard-status">

            <span class="status-dot"></span>

            <span>
                Dataset Loaded
            </span>

        </div>

    </section>


    <!-- ================================================== -->
    <!-- DATASET UPLOAD -->
    <!-- ================================================== -->

    <section class="dashboard-card dataset-upload-card">

        <div class="card-header">

            <div>

                <p class="card-eyebrow">
                    DATASET
                </p>

                <h2>
                    Upload Sales Data
                </h2>

                <p class="card-description">
                    Drag and drop an Excel file here or select one
                    from your computer.
                </p>

            </div>

        </div>


        <div
            id="datasetDropZone"
            class="dataset-drop-zone"
        >

            <div class="dataset-upload-icon">
                📄
            </div>

            <div class="dataset-upload-title">
                Drag & Drop Excel File
            </div>

            <div class="dataset-upload-description">
                or click to browse
            </div>

            <div class="dataset-upload-supported">
                Supports .xlsx and .xls files
            </div>

            <input
                type="file"
                id="datasetFileInput"
                accept=".xlsx,.xls"
                hidden
            >

        </div>


        <div
            id="datasetUploadStatus"
            class="dataset-upload-status"
            style="display: none;"
        ></div>

    </section>


    <!-- ================================================== -->
    <!-- KPI CARDS -->
    <!-- ================================================== -->

    <section class="kpi-grid">

        <div class="kpi-card">

            <div class="kpi-card-header">

                <span class="kpi-label">
                    Total Units Sold
                </span>

                <span class="kpi-icon">
                    ↗️
                </span>

            </div>

            <div
                class="kpi-value"
                id="totalUnits"
            >
                —
            </div>

            <div class="kpi-description">
                Total sales volume
            </div>

        </div>


        <div class="kpi-card">

            <div class="kpi-card-header">

                <span class="kpi-label">
                    Total Records
                </span>

                <span class="kpi-icon">
                    #
                </span>

            </div>

            <div
                class="kpi-value"
                id="totalRecords"
            >
                —
            </div>

            <div class="kpi-description">
                Sales records processed
            </div>

        </div>


        <div class="kpi-card">

            <div class="kpi-card-header">

                <span class="kpi-label">
                    Devices
                </span>

                <span class="kpi-icon">
                    ◇
                </span>

            </div>

            <div
                class="kpi-value"
                id="uniqueDevices"
            >
                —
            </div>

            <div class="kpi-description">
                Unique devices sold
            </div>

        </div>


        <div class="kpi-card">

            <div class="kpi-card-header">

                <span class="kpi-label">
                    Dealers
                </span>

                <span class="kpi-icon">
                    ◎
                </span>

            </div>

            <div
                class="kpi-value"
                id="uniqueDealers"
            >
                —
            </div>

            <div class="kpi-description">
                Active dealers
            </div>

        </div>

    </section>


    <!-- ================================================== -->
    <!-- MAIN DASHBOARD -->
    <!-- ================================================== -->

    <section class="dashboard-grid">


        <!-- SALES OVERVIEW -->

        <div class="dashboard-card sales-overview">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        PERFORMANCE
                    </p>

                    <h2>
                        Sales Overview
                    </h2>

                </div>

                <button
                    class="card-action"
                    type="button"
                >
                    View Details
                </button>

            </div>


            <div class="chart-placeholder">

                <div class="chart-placeholder-content">

                    <span class="chart-placeholder-icon">
                        ↗️
                    </span>

                    <h3>
                        Sales Trend
                    </h3>

                    <p>
                        Monthly sales performance will appear here.
                    </p>

                </div>

            </div>

        </div>


        <!-- TOP DEVICE -->

        <div class="dashboard-card">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        PRODUCT
                    </p>

                    <h2>
                        Best Selling Device
                    </h2>

                </div>

            </div>


            <div class="insight-content">

                <div class="insight-label">
                    TOP DEVICE
                </div>

                <div
                    class="insight-value"
                    id="topDevice"
                >
                    Loading...
                </div>

                <div
                    class="insight-metric"
                    id="topDeviceUnits"
                >
                    —
                </div>

                <div class="insight-description">
                    Units sold
                </div>

            </div>

        </div>


        <!-- TOP DEALER -->

        <div class="dashboard-card">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        DEALER
                    </p>

                    <h2>
                        Best Performing Dealer
                    </h2>

                </div>

            </div>


            <div class="insight-content">

                <div class="insight-label">
                    TOP DEALER
                </div>

                <div
                    class="insight-value"
                    id="topDealer"
                >
                    Loading...
                </div>

                <div
                    class="insight-metric"
                    id="topDealerUnits"
                >
                    —
                </div>

                <div class="insight-description">
                    Units sold
                </div>

            </div>

        </div>


        <!-- TOP REGION -->

        <div class="dashboard-card">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        GEOGRAPHY
                    </p>

                    <h2>
                        Highest Sales Region
                    </h2>

                </div>

            </div>


            <div class="insight-content">

                <div class="insight-label">
                    TOP REGION
                </div>

                <div
                    class="insight-value"
                    id="topRegion"
                >
                    Loading...
                </div>

                <div
                    class="insight-metric"
                    id="topRegionUnits"
                >
                    —
                </div>

                <div class="insight-description">
                    Units sold
                </div>

            </div>

        </div>


        <!-- TOP STATE -->

        <div class="dashboard-card">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        GEOGRAPHY
                    </p>

                    <h2>
                        Highest Sales State
                    </h2>

                </div>

            </div>


            <div class="insight-content">

                <div class="insight-label">
                    TOP STATE
                </div>

                <div
                    class="insight-value"
                    id="topState"
                >
                    Loading...
                </div>

                <div
                    class="insight-metric"
                    id="topStateUnits"
                >
                    —
                </div>

                <div class="insight-description">
                    Units sold
                </div>

            </div>

        </div>


        <!-- BEST MONTH -->

        <div class="dashboard-card">

            <div class="card-header">

                <div>

                    <p class="card-eyebrow">
                        MONTHLY PERFORMANCE
                    </p>

                    <h2>
                        Best Month
                    </h2>

                </div>

            </div>


            <div class="insight-content">

                <div class="insight-label">
                    PEAK SALES
                </div>

                <div
                    class="insight-value"
                    id="bestMonth"
                >
                    Loading...
                </div>

                <div
                    class="insight-metric"
                    id="bestMonthUnits"
                >
                    —
                </div>

                <div class="insight-description">
                    Units sold
                </div>

            </div>

        </div>


    </section>


    <!-- ================================================== -->
    <!-- AI QUERY -->
    <!-- ================================================== -->

    <section class="dashboard-card ai-query-card">

        <div class="card-header">

            <div>

                <p class="card-eyebrow">
                    AI ANALYTICS
                </p>

                <h2>
                    Ask Sales & Inventory AI
                </h2>

                <p class="card-description">
                    Select a question from the available analytics
                    instead of typing it manually.
                </p>

            </div>

        </div>


        <div class="ai-question-selector">

            <div
                id="dashboardQuestion"
                class="ai-question-selector-display"
            >
                Select a question to begin...
            </div>


            <button
                type="button"
                id="dashboardQuestionButton"
                class="ai-question-selector-button"
            >
                Ask AI
            </button>


            <button
                type="button"
                id="dashboardQuestionReset"
                class="ai-question-reset-button"
            >
                Reset
            </button>

        </div>


        <div
            id="dashboardResponse"
            class="ai-response"
            style="display: none;"
        >

            <div class="ai-response-header">

                <span class="ai-response-label">
                    AI RESPONSE
                </span>

            </div>

            <div
                id="dashboardResponseText"
                class="ai-response-text"
            ></div>

        </div>

    </section>


</div>


<!-- ========================================================= -->
<!-- AI QUESTION MODAL -->
<!-- ========================================================= -->

<div
    id="aiQuestionModal"
    class="ai-question-modal"
    aria-hidden="true"
>

    <div
        class="ai-question-modal-content"
        role="dialog"
        aria-modal="true"
        aria-labelledby="aiQuestionModalTitle"
    >


        <!-- MODAL HEADER -->

        <div class="ai-question-modal-header">

            <div class="ai-question-modal-header-left">

                <p class="ai-question-modal-eyebrow">
                    AI ANALYTICS
                </p>

                <h2
                    id="aiQuestionModalTitle"
                    class="ai-question-modal-title"
                >
                    Choose a Question
                </h2>

                <p class="ai-question-modal-description">
                    Select a question from the analytics available
                    in your Sales & Inventory system.
                </p>

            </div>


            <button
                type="button"
                id="aiQuestionModalClose"
                class="ai-question-modal-close"
                aria-label="Close question selector"
            >
                ×
            </button>

        </div>


        <!-- SEARCH -->

        <div class="ai-question-search-wrapper">

            <span
                class="ai-question-search-icon"
                aria-hidden="true"
            >
                🔍
            </span>

            <input
                type="text"
                id="aiQuestionSearch"
                class="ai-question-search"
                placeholder="Search questions..."
                autocomplete="off"
            >

        </div>


        <!-- QUESTION LIST -->

        <div
            id="aiQuestionList"
            class="ai-question-list"
        ></div>


        <!-- EMPTY SEARCH -->

        <div
            id="aiQuestionEmpty"
            class="ai-question-empty"
        >

            <div class="ai-question-empty-icon">
                🔍
            </div>

            <h3>
                No questions found
            </h3>

            <p>
                Try searching with a different keyword.
            </p>

        </div>


        <!-- FOOTER -->

        <div class="ai-question-modal-footer">

            <span
                id="aiQuestionCount"
                class="ai-question-count"
            >
                0 questions
            </span>

            <button
                type="button"
                id="aiQuestionCancel"
                class="ai-question-cancel"
            >
                Cancel
            </button>

        </div>


    </div>

</div>


{% endblock %}


{% block extra_js %}

<script>

/* ============================================================
   DASHBOARD INITIALIZATION
   ============================================================ */

function initializeDashboard() {

    console.log(
        "Sales & Inventory AI dashboard initialized."
    );

    loadDashboardData();

    setupAIQuery();

    setupDatasetUpload();

}


/* ============================================================
   LOAD DASHBOARD DATA
   ============================================================ */

async function loadDashboardData() {

    try {

        console.log(
            "Loading dashboard data..."
        );


        const response = await fetch(
            "/api/query",
            {
                method: "POST",

                headers: {
                    "Content-Type": "application/json"
                },

                body: JSON.stringify({
                    question:
                        "Give me an overall sales summary."
                })
            }
        );


        if (!response.ok) {

            throw new Error(
                `API request failed with status ${response.status}`
            );

        }


        const data =
            await response.json();


        console.log(
            "Overall dashboard response:",
            data
        );


        if (!data.success) {

            console.error(
                "Dashboard API error:",
                data.error
            );

            return;

        }


        const result =
            data.result || {};


        document.getElementById(
            "totalUnits"
        ).textContent =
            Number(
                result.total_units || 0
            ).toLocaleString();


        document.getElementById(
            "totalRecords"
        ).textContent =
            Number(
                result.total_records || 0
            ).toLocaleString();


        document.getElementById(
            "uniqueDevices"
        ).textContent =
            Number(
                result.unique_devices || 0
            ).toLocaleString();


        document.getElementById(
            "uniqueDealers"
        ).textContent =
            Number(
                result.unique_dealers || 0
            ).toLocaleString();


        await Promise.all([
            loadInsight(
                "What is the best selling device?"
            ),

            loadInsight(
                "Who is the best dealer?"
            ),

            loadInsight(
                "Which region has the highest sales?"
            ),

            loadInsight(
                "Which state has the highest sales?"
            ),

            loadInsight(
                "What was the best month?"
            )
        ]);


        console.log(
            "Dashboard insights loaded."
        );

    }
    catch (error) {

        console.error(
            "Failed to load dashboard:",
            error
        );

    }

}


/* ============================================================
   LOAD INDIVIDUAL INSIGHT
   ============================================================ */

async function loadInsight(question) {

    try {

        console.log(
            "Loading insight:",
            question
        );


        const response = await fetch(
            "/api/query",
            {
                method: "POST",

                headers: {
                    "Content-Type": "application/json"
                },

                body: JSON.stringify({
                    question: question
                })
            }
        );


        if (!response.ok) {

            throw new Error(
                `Insight API request failed with status ${response.status}`
            );

        }


        const data =
            await response.json();


        console.log(
            "Insight response:",
            question,
            data
        );


        if (!data.success) {

            console.error(
                "Insight API error:",
                data.error
            );

            return;

        }


        const result =
            data.result || {};


        if (
            data.intent === "top_device"
        ) {

            document.getElementById(
                "topDevice"
            ).textContent =
                result.device_name || "—";


            document.getElementById(
                "topDeviceUnits"
            ).textContent =
                Number(
                    result.units || 0
                ).toLocaleString();

        }


        if (
            data.intent === "top_dealer"
        ) {

            document.getElementById(
                "topDealer"
            ).textContent =
                result.dealer_name || "—";


            document.getElementById(
                "topDealerUnits"
            ).textContent =
                Number(
                    result.units || 0
                ).toLocaleString();

        }


        if (
            data.intent === "top_region"
        ) {

            document.getElementById(
                "topRegion"
            ).textContent =
                result.region || "—";


            document.getElementById(
                "topRegionUnits"
            ).textContent =
                Number(
                    result.units || 0
                ).toLocaleString();

        }


        if (
            data.intent === "top_state"
        ) {

            document.getElementById(
                "topState"
            ).textContent =
                result.state || "—";


            document.getElementById(
                "topStateUnits"
            ).textContent =
                Number(
                    result.units || 0
                ).toLocaleString();

        }


        if (
            data.intent === "best_month"
        ) {

            document.getElementById(
                "bestMonth"
            ).textContent =
                `${result.month || "—"} ${result.year || ""}`;


            document.getElementById(
                "bestMonthUnits"
            ).textContent =
                Number(
                    result.units || 0
                ).toLocaleString();

        }

    }
    catch (error) {

        console.error(
            "Failed to load insight:",
            question,
            error
        );

    }

}


/* ============================================================
   DATASET UPLOAD
   ============================================================ */

function setupDatasetUpload() {

    const dropZone =
        document.getElementById(
            "datasetDropZone"
        );

    const fileInput =
        document.getElementById(
            "datasetFileInput"
        );

    const uploadStatus =
        document.getElementById(
            "datasetUploadStatus"
        );


    if (
        !dropZone ||
        !fileInput ||
        !uploadStatus
    ) {

        console.error(
            "Dataset upload elements were not found."
        );

        return;

    }


    dropZone.addEventListener(
        "click",
        function () {

            fileInput.click();

        }
    );


    fileInput.addEventListener(
        "change",
        function () {

            if (
                fileInput.files &&
                fileInput.files.length > 0
            ) {

                uploadDataset(
                    fileInput.files[0]
                );

            }

        }
    );


    dropZone.addEventListener(
        "dragover",
        function (event) {

            event.preventDefault();

            dropZone.classList.add(
                "drag-over"
            );

        }
    );


    dropZone.addEventListener(
        "dragleave",
        function () {

            dropZone.classList.remove(
                "drag-over"
            );

        }
    );


    dropZone.addEventListener(
        "drop",
        function (event) {

            event.preventDefault();

            dropZone.classList.remove(
                "drag-over"
            );


            const files =
                event.dataTransfer.files;


            if (
                files &&
                files.length > 0
            ) {

                uploadDataset(
                    files[0]
                );

            }

        }
    );


    async function uploadDataset(file) {

        if (!file) {

            return;

        }


        const filename =
            file.name.toLowerCase();


        if (
            !filename.endsWith(".xlsx") &&
            !filename.endsWith(".xls")
        ) {

            uploadStatus.textContent =
                "Invalid file type. Please upload an Excel file.";

            uploadStatus.style.display =
                "flex";

            return;

        }


        uploadStatus.textContent =
            `Uploading ${file.name}...`;

        uploadStatus.style.display =
            "flex";


        const formData =
            new FormData();


        formData.append(
            "file",
            file
        );


        try {

            const response =
                await fetch(
                    "/api/upload",
                    {
                        method: "POST",
                        body: formData
                    }
                );


            const data =
                await response.json();


            if (!response.ok || !data.success) {

                let errorMessage =
                    data.error ||
                    "Failed to upload dataset.";


                if (
                    data.missing_columns &&
                    data.missing_columns.length > 0
                ) {

                    errorMessage +=
                        " Missing columns: " +
                        data.missing_columns.join(
                            ", "
                        );

                }


                throw new Error(
                    errorMessage
                );

            }


            uploadStatus.textContent =
                `Dataset loaded successfully: ${data.filename} (${Number(data.rows).toLocaleString()} rows)`;


            console.log(
                "Dataset uploaded successfully:",
                data
            );


            await loadDashboardData();

        }
        catch (error) {

            console.error(
                "Dataset upload failed:",
                error
            );


            uploadStatus.textContent =
                error.message ||
                "Failed to upload dataset.";

        }

    }

}


/* ============================================================
   PREDEFINED AI QUESTIONS
   ============================================================ */

const predefinedAIQuestions = [

    {
        category: "Sales Overview",

        questions: [
            {
                text:
                    "What is the overall sales summary?"
            },

            {
                text:
                    "What is the overall sales performance?"
            },

            {
                text:
                    "Give me an overall sales overview."
            }
        ]
    },


    {
        category: "Devices",

        questions: [
            {
                text:
                    "What is the best selling device?"
            },

            {
                text:
                    "What are the top 5 devices?"
            },

            {
                text:
                    "What are the top 10 devices?"
            },

            {
                text:
                    "Which device has the highest sales?"
            }
        ]
    },


    {
        category: "Dealers",

        questions: [
            {
                text:
                    "Who is the best dealer?"
            },

            {
                text:
                    "What are the top 5 dealers?"
            },

            {
                text:
                    "What are the top 10 dealers?"
            },

            {
                text:
                    "Which dealer has the highest sales performance?"
            }
        ]
    },


    {
        category: "Geography",

        questions: [
            {
                text:
                    "Which region has the highest sales?"
            },

            {
                text:
                    "Which state has the highest sales?"
            },

            {
                text:
                    "What is the top performing region?"
            },

            {
                text:
                    "What is the top performing state?"
            }
        ]
    },


    {
        category: "Monthly Performance",

        questions: [
            {
                text:
                    "What was the best month?"
            },

            {
                text:
                    "What was the worst month?"
            },

            {
                text:
                    "What is the latest month's sales performance?"
            },

            {
                text:
                    "What is the latest month's change?"
            },

            {
                text:
                    "What was the biggest monthly decline?"
            }
        ]
    },


    {
        category: "Recontract",

        questions: [
            {
                text:
                    "What is the recontract sales performance?"
            },

            {
                text:
                    "What percentage of sales are recontract?"
            },

            {
                text:
                    "What are the new device GA sales?"
            }
        ]
    },


    {
        category: "Sales Structure",

        questions: [
            {
                text:
                    "Which sales channel has the highest sales?"
            },

            {
                text:
                    "Which Rateplan has the highest sales?"
            },

            {
                text:
                    "Which Baseplan has the highest sales?"
            },

            {
                text:
                    "Which customer subtype has the highest sales?"
            }
        ]
    },


    {
        category: "Dealer Information",

        questions: [
            {
                text:
                    "What is the dealer code?"
            }
        ]
    }

];


/* ============================================================
   AI QUERY
   ============================================================ */

function setupAIQuery() {

    const questionDisplay =
        document.getElementById(
            "dashboardQuestion"
        );

    const questionButton =
        document.getElementById(
            "dashboardQuestionButton"
        );

    const resetButton =
        document.getElementById(
            "dashboardQuestionReset"
        );

    const responseBox =
        document.getElementById(
            "dashboardResponse"
        );

    const responseText =
        document.getElementById(
            "dashboardResponseText"
        );

    const modal =
        document.getElementById(
            "aiQuestionModal"
        );

    const modalClose =
        document.getElementById(
            "aiQuestionModalClose"
        );

    const modalCancel =
        document.getElementById(
            "aiQuestionCancel"
        );

    const searchInput =
        document.getElementById(
            "aiQuestionSearch"
        );

    const questionList =
        document.getElementById(
            "aiQuestionList"
        );

    const emptyState =
        document.getElementById(
            "aiQuestionEmpty"
        );

    const questionCount =
        document.getElementById(
            "aiQuestionCount"
        );


    if (
        !questionDisplay ||
        !questionButton ||
        !resetButton ||
        !responseBox ||
        !responseText ||
        !modal ||
        !modalClose ||
        !modalCancel ||
        !searchInput ||
        !questionList ||
        !emptyState ||
        !questionCount
    ) {

        console.error(
            "AI query elements were not found."
        );

        return;

    }


    let selectedQuestion = "";


    /* ========================================================
       GET ALL QUESTIONS
       ======================================================== */

    function getAllQuestions() {

        const questions = [];

        predefinedAIQuestions.forEach(
            function (category) {

                category.questions.forEach(
                    function (question) {

                        questions.push({
                            category:
                                category.category,

                            text:
                                question.text
                        });

                    }
                );

            }
        );

        return questions;

    }


    /* ========================================================
       RENDER QUESTIONS
       ======================================================== */

    function renderQuestions(searchTerm = "") {

        questionList.innerHTML = "";

        const normalizedSearch =
            searchTerm
                .trim()
                .toLowerCase();


        let visibleQuestionCount = 0;


        predefinedAIQuestions.forEach(
            function (category) {

                const matchingQuestions =
                    category.questions.filter(
                        function (question) {

                            if (!normalizedSearch) {

                                return true;

                            }

                            return question.text
                                .toLowerCase()
                                .includes(
                                    normalizedSearch
                                );

                        }
                    );


                if (
                    matchingQuestions.length === 0
                ) {

                    return;

                }


                visibleQuestionCount +=
                    matchingQuestions.length;


                const categoryContainer =
                    document.createElement(
                        "div"
                    );

                categoryContainer.className =
                    "ai-question-category";


                const categoryTitle =
                    document.createElement(
                        "div"
                    );

                categoryTitle.className =
                    "ai-question-category-title";

                categoryTitle.textContent =
                    category.category;


                categoryContainer.appendChild(
                    categoryTitle
                );


                matchingQuestions.forEach(
                    function (question) {

                        const questionButton =
                            document.createElement(
                                "button"
                            );

                        questionButton.type =
                            "button";

                        questionButton.className =
                            "ai-question-item";


                        const questionText =
                            document.createElement(
                                "span"
                            );

                        questionText.className =
                            "ai-question-item-text";

                        questionText.textContent =
                            question.text;


                        const arrow =
                            document.createElement(
                                "span"
                            );

                        arrow.className =
                            "ai-question-item-arrow";

                        arrow.textContent =
                            "→";


                        questionButton.appendChild(
                            questionText
                        );

                        questionButton.appendChild(
                            arrow
                        );


                        questionButton.addEventListener(
                            "click",
                            function () {

                                selectQuestion(
                                    question.text
                                );

                            }
                        );


                        categoryContainer.appendChild(
                            questionButton
                        );

                    }
                );


                questionList.appendChild(
                    categoryContainer
                );

            }
        );


        if (
            visibleQuestionCount === 0
        ) {

            questionList.style.display =
                "none";

            emptyState.style.display =
                "block";

        }
        else {

            questionList.style.display =
                "block";

            emptyState.style.display =
                "none";

        }


        questionCount.textContent =
            `${visibleQuestionCount} ${
                visibleQuestionCount === 1
                    ? "question"
                    : "questions"
            }`;

    }


    /* ========================================================
       SELECT QUESTION
       ======================================================== */

    function selectQuestion(question) {

        selectedQuestion =
            question;


        questionDisplay.textContent =
            question;


        questionDisplay.classList.add(
            "has-question"
        );


        closeQuestionModal();


        responseBox.style.display =
            "none";

    }


    /* ========================================================
       RESET AI SECTION
       ======================================================== */

    function resetAIQuery() {

        selectedQuestion =
            "";


        questionDisplay.textContent =
            "Select a question to begin...";


        questionDisplay.classList.remove(
            "has-question"
        );


        responseText.textContent =
            "";


        responseBox.style.display =
            "none";


        questionButton.disabled =
            false;


        questionButton.textContent =
            "Ask AI";


        console.log(
            "AI query section reset."
        );

    }


    /* ========================================================
       OPEN MODAL
       ======================================================== */

    function openQuestionModal() {

        renderQuestions();

        searchInput.value = "";

        modal.classList.add(
            "active"
        );

        modal.setAttribute(
            "aria-hidden",
            "false"
        );

        document.body.classList.add(
            "ai-question-modal-open"
        );


        setTimeout(
            function () {

                searchInput.focus();

            },
            50
        );

    }


    /* ========================================================
       CLOSE MODAL
       ======================================================== */

    function closeQuestionModal() {

        modal.classList.remove(
            "active"
        );

        modal.setAttribute(
            "aria-hidden",
            "true"
        );

        document.body.classList.remove(
            "ai-question-modal-open"
        );

    }


    /* ========================================================
       ASK AI
       ======================================================== */

    async function askAI() {

        if (!selectedQuestion) {

            openQuestionModal();

            return;

        }


        questionButton.disabled =
            true;

        questionButton.textContent =
            "Thinking...";


        responseBox.style.display =
            "none";


        try {

            const response =
                await fetch(
                    "/api/query",
                    {
                        method: "POST",

                        headers: {
                            "Content-Type":
                                "application/json"
                        },

                        body:
                            JSON.stringify({
                                question:
                                    selectedQuestion
                            })
                    }
                );


            if (!response.ok) {

                throw new Error(
                    `AI API request failed with status ${response.status}`
                );

            }


            const data =
                await response.json();


            if (!data.success) {

                responseText.textContent =
                    data.error ||
                    "Unable to process your question.";

            }
            else {

                responseText.textContent =
                    data.response ||
                    "No response returned.";

            }


            responseBox.style.display =
                "block";

        }
        catch (error) {

            console.error(
                "AI query failed:",
                error
            );

            responseText.textContent =
                "Unable to connect to the AI service.";

            responseBox.style.display =
                "block";

        }
        finally {

            questionButton.disabled =
                false;

            questionButton.textContent =
                "Ask AI";

        }

    }


    /* ========================================================
       OPEN QUESTION SELECTOR
       ======================================================== */

    questionButton.addEventListener(
        "click",
        function () {

            if (!selectedQuestion) {

                openQuestionModal();

                return;

            }

            askAI();

        }
    );


    /* ========================================================
       RESET BUTTON
       ======================================================== */

    resetButton.addEventListener(
        "click",
        function () {

            resetAIQuery();

        }
    );


    /* ========================================================
       CLOSE BUTTON
       ======================================================== */

    modalClose.addEventListener(
        "click",
        closeQuestionModal
    );


    modalCancel.addEventListener(
        "click",
        closeQuestionModal
    );


    /* ========================================================
       SEARCH
       ======================================================== */

    searchInput.addEventListener(
        "input",
        function () {

            renderQuestions(
                searchInput.value
            );

        }
    );


    /* ========================================================
       CLOSE WHEN CLICKING OUTSIDE MODAL
       ======================================================== */

    modal.addEventListener(
        "click",
        function (event) {

            if (
                event.target === modal
            ) {

                closeQuestionModal();

            }

        }
    );


    /* ========================================================
       ESCAPE KEY
       ======================================================== */

    document.addEventListener(
        "keydown",
        function (event) {

            if (
                event.key === "Escape" &&
                modal.classList.contains(
                    "active"
                )
            ) {

                closeQuestionModal();

            }

        }
    );


    /* ========================================================
       INITIAL QUESTION LIST
       ======================================================== */

    renderQuestions();

}


/* ============================================================
   START DASHBOARD
   ============================================================ */

initializeDashboard();

</script>

{% endblock %}
