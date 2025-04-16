DISM /Online /Cleanup-Image /CheckHealth
sfc /scannow
DISM /Online /Cleanup-Image /ScanHealth
sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
sfc /scannow
DISM /Online /Cleanup-Image /StartComponentCleanup
sfc /scannow
DISM /Online /Cleanup-Image /AnalyzeComponentStore (существует только на вин 10, на других будет ошибка 87)
sfc /scannow