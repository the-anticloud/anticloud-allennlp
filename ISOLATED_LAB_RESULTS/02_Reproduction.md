# Reproduction — ACADEMIA_RD/ALLENNLP

```bat
cd /d E:\fenta\Downloads\The Anticloud\ANTICLOUD_REPOS\ACADEMIA_RD\ALLENNLP
python tools\run_bench.py --out BENCH.json --quiet
python -c "import json;d=json.load(open('BENCH.json'));print(d['all_passed'],d['passed'],'/',d['total'])"
```

Last run aggregate: 16/16 (PASS); evidence SHA3-256 `a57794de6c0a73d6f4dd67bf082ede567c6ea195ed6a8a94a1a89d4679002624`.
