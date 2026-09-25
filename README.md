# Osteosarcoma HLA-II analysis code

Analysis code and processed research tables supporting:

**Disentangling HLA-II expression in osteosarcoma: an osteogenic RNA gradient and its myeloid-dominant protein context**

## Public access

This repository and its release assets are publicly accessible. The manuscript version is the [code-package-20260906 release](https://github.com/nagasaki-miku/osteosarcoma-hlaii-code/releases/tag/code-package-20260906). Public access was enabled on 2026-09-25.

The original archive is preserved with its existing checksum. Statements inside that dated snapshot about a repository not yet being assigned describe the preparation stage; the links on this page provide the current access route. No software license or DOI is assigned by this visibility change.

## Download the complete code package

The complete **702-file** package is distributed as a **Release asset** to preserve the full directory hierarchy. Open **Releases** in this repository and download:

- `osteosarcoma-hlaii-code_20260906.zip` (approximately 59.2 MiB)
- `osteosarcoma-hlaii-code_20260906.zip.sha256`

The repository's automatic **Source code (zip)** download contains this landing page; use the explicitly named release asset above for the full analysis package.

Archive SHA-256:

```text
fa3c7f49b8104b4fb8791f6f95293003e561ff645bbcf62b66539842ca8a7380
```

After extraction, enter the `osteosarcoma-hlaii-code` directory. It contains the analysis scripts, compact processed tables, English and Chinese READMEs, dependency versions, figure-to-source mapping, privacy-scope description and per-file checksums.

## Minimum reproduction

Use Python 3.12 and run the following commands from the extracted package root:

```bash
python -m pip install -r requirements-minimal.txt
python scripts/verify_package.py
python scripts/reproduce_t2.py
python scripts/reproduce_figure6.py
```

The T2 command recomputes all 5 primary tests, 35 sensitivity tests, 45 descriptive checks and 25 quintile-summary rows from the frozen paired measurements of 509 cells. All four result tables matched the original results exactly during preparation. The Figure 6 command rebuilds the current figure using all 509 paired cells and the published UMAP coordinates.

The archive includes 110 Python and 8 R files. The entire original-data-to-manuscript workflow was not rerun in a fresh environment. See the package's `docs/REPRODUCIBILITY.md` for the verified scope and remaining external inputs.

## Privacy and distribution status

The release contains the separately screened code package. Direct author/contact information, machine-specific account paths, credential files, environment/configuration snapshots, Git history, original Office documents and local audit records are excluded. Public dataset accessions, pseudonymous sample identifiers and cell barcodes are retained for scientific joins. Package preparation did not change scientific numeric table values.

No software license has been selected, and no archival DOI has been assigned. See `RIGHTS.md`.

## 中文使用说明

完整代码和数据位于 **Releases** 中的 `osteosarcoma-hlaii-code_20260906.zip`，共 702 个文件。请下载该附件并解压，再阅读包内 `README_zh.md`。GitHub 自动生成的 **Source code (zip)** 仅包含本仓库首页文件，不是完整研究代码包。

仓库及 Release 附件已于 2026-09-25 公开，可直接查看和下载，无需向通讯作者申请访问。最小复现从冻结的 509 个细胞的处理后配对数据开始，整篇论文的原始数据全流程并未在本次重新运行。
