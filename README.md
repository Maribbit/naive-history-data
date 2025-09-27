# Naive History Data

Visualization: [Naive History App](https://maribbit.github.io/naive-history-app/).

## Overview | 概述

The aim of this dataset is to compare the historical development of different civilizations. Therefore, the selection of events needs to consider multiple dimensions such as themes, time density, and event significance, with a preference for events that have clear time points.

The complexity of the construction process exceeded my expectations. To create a preliminary usable version, I extensively utilized large language models (LLMs) to generate and organize the data, which obviously lacks verification and rigor. If you find any errors, please feel free to submit an issue with references.

本数据集的构建目标是为了对比不同文明的历史发展脉络，因此事件的选择需要在主题、时间密度、事件重要性等维度上进行综合考虑，并且优先选择具有明确时间节点的事件。

构建过程的复杂性超出了我的预期。因此为了能够做出一个初步可用的版本，我大量使用了大语言模型（LLM）来生成和整理数据，这显然缺少佐证和严谨性。如果您发现错误，欢迎您提交Issue，并附上参考文献。

## Technical Overview | 技术概述

This dataset is in JSON format, containing two parts: events and tags, with references to events on the tags.

The meanings of other fields are self-explanatory. All text that needs to be displayed supports both Chinese and English.

I have developed an NPM package [fuzzy-date-ts](https://www.npmjs.com/package/fuzzy-date-ts) specifically to handle fuzzy dates. The dates here are all serialized products of this package.

本数据集采用 JSON 格式，包含事件和标签两部分数据，标签上有对事件的引用。

其余字段的含义不言自明。所有需要显示的文字均支持中英双语。

我专门开发了一个NPM包 [fuzzy-date-ts](https://www.npmjs.com/package/fuzzy-date-ts) 来处理模糊日期。这里的日期均为此包的序列化产物。

## Development | 发展

If you have any questions or suggestions, please feel free to open an issue.

如果您有任何问题或建议，欢迎随时提交Issue。

Adding new events requires references and a balanced consideration. This kind of issue might be rejected.

新增事件需要有参考文献，并且需要考虑数据集的平衡性。这类Issue可能会被拒绝。

I **do not accept** requests to modify data for subjective reasons such as preferences, political stance, values, etc.

我**不接受**因为喜好、政治立场、价值观等主观原因而要求修改数据的请求。

If you give Maribbit a star, you are welcome to join the QQ Group: 1059966304

给海兔一个⭐️，欢迎加入企鹅群：1059966304

## Contributing | 贡献

Want to add or improve references? See the [Contributing Guide](CONTRIBUTING.md) for a step-by-step walkthrough, including tips for newcomers to GitHub.

想为事件补充或完善参考文献？请阅读 [贡献指南](CONTRIBUTING.md)，其中包含详细的操作步骤和对新手友好的说明。

## License | 许可证

This dataset is licensed under [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to use, share, and adapt this dataset for any purpose, including commercial use, as long as you provide appropriate attribution.

该数据集采用 [知识共享署名 4.0 国际许可协议 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.zh) 进行许可。

您可以自由地使用、共享和修改此数据集，包括用于商业目的，只需提供适当的署名即可。

## Citation | 引用

If you use this dataset in your research or project, please cite it as:

```
Maribbit. (2025). Naive History Data. Retrieved from https://github.com/Maribbit/naive-history-data
```

如果您在研究或项目中使用此数据集，请按以下格式引用：

```
Maribbit. (2025). Naive History Data. Retrieved from https://github.com/Maribbit/naive-history-data
```