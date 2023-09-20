# Nim Compiler as GitHub action

![build](https://img.shields.io/github/workflow/status/skynet-core/nim/main?style=for-the-badge)
![downloads](https://img.shields.io/github/downloads/skynet-core/nim/total?style=for-the-badge)
![last commit](https://img.shields.io/github/last-commit/skynet-core/nim?style=for-the-badge)
![last release](https://img.shields.io/github/release-date/skynet-core/nim?color=red&logoColor=green&style=for-the-badge)

Nim language compiler and tools within Alpine 3.12 image built with musl.

```
Will use nim 1.6.14
```

## Inputs

### `command`

**Optional** Command to run. Default is `nimble build --nimcache:/tmp/.cache --nimbleDir:/tmp/.nimble --gcc.exe:gcc --gcc.linkerexe:gcc --passL:-static -d:release --opt:size -y`

## Example usage

Run tests and set `STATUS` output variable

    - name: Run tests
      uses: skynet-core/nim@v1.2
      id: nim-test
      with:
        command: 'nimble build --nimcache:/tmp/.cache --nimbleDir:/tmp/.nimble --gcc.exe:gcc --gcc.linkerexe:gcc --passL:-static -d:release --opt:size -y'
