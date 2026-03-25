# MLX91805-Payload

MLX91805 TPMS 传感器轮胎载荷检测 - CPR 完整推导文档

## 内容

- **[cpr_load_derivation.html](./cpr_load_derivation.html)** - 完整的 CPR 推导与载荷计算交互式文档

### 包含内容

1. 轮胎接触弧检测原理（SVG 动画可视化）
2. `Tms_DetectPatchesZ()` 所有 9 个参数的完整推导
   - `sampling_period_us` 推导（轮胎参数 → 接地弧长 → 采样周期）
   - `detection_threshold` 自适应阈值推导
   - `ntimeout` 超时点数推导
3. 索引 → CPR 完整数学推导（定点整数化）
4. CPR → 载荷线性标定推导（两点标定法）
5. 交互计算器：CPR 计算 + 两点标定 + 载荷实时估算
6. 双无线通信架构（RF 433MHz 上行 + LF 125kHz 下行）
7. NVRAM 16 字节存储格式

## 硬件

- 传感器芯片：[迈来芯 MLX91805](https://www.melexis.com/en/product/MLX91805)
- 架构：MLX16，使用 mlx16-elf-gcc 工具链
- 通信：RF 433MHz（传感器→PC）+ LF 125kHz（PC→传感器）

## License

MIT
