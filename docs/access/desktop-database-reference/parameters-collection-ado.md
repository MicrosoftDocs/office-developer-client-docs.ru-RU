---
title: Коллекция параметров (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287946"
---
# <a name="parameters-collection-ado"></a>Коллекция параметров (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все [объекты Параметр](parameter-object-ado.md) объекта [Command.](command-object-ado.md)

## <a name="remarks"></a>Примечания

Объект **Command** имеет коллекцию **Параметры,** которая состоит из **объектов Parameter.**

С помощью метода  [Обновления](refresh-method-ado.md) в  коллекции Параметры объекта Command извлекает сведения о параметрах поставщика для сохраненной процедуры или параметризованного запроса, указанного в **объекте Command.** Некоторые поставщики не поддерживают сохраненные вызовы процедур или параметризированные запросы; вызов метода **Обновления** в коллекции **Параметры** при использовании такого поставщика возвращает ошибку.

Если вы не определили собственные объекты **Parameter** и получили  доступ к коллекции **Параметры** перед вызовом метода Обновления, ADO автоматически вызывает метод и заполняет коллекцию для вас.

Вы можете свести к минимуму вызовы к поставщику для повышения производительности, если вы знаете свойства параметров, связанных с хранимой процедурой или параметризированным запросом, который вы хотите вызвать. Используйте метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Параметры** с соответствующими параметрами свойств и используйте метод [Append,](append-method-ado.md) чтобы добавить их в коллекцию **Параметры.** Это позволяет устанавливать и возвращать значения параметров, не вызывая поставщика для получения сведений о параметрах. Если вы пишете поставщику, который не поставляет сведения о  параметрах, необходимо вручную заполнить коллекцию Параметры с помощью этого метода, чтобы иметь возможность использовать параметры вообще. При необходимости используйте метод [Delete,](delete-method-ado-parameters-collection.md) чтобы удалить **объекты Parameter** из коллекции **Параметры.**

Объекты из коллекции **Параметры** в **наборе Recordset** выйдут из области (поэтому становятся недоступными) при закрытии **recordset.**

