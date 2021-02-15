---
title: Коллекция Parameters (ADO)
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
# <a name="parameters-collection-ado"></a>Коллекция Parameters (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все [объекты Parameter](parameter-object-ado.md) объекта [Command.](command-object-ado.md)

## <a name="remarks"></a>Заметки

Объект **Command** имеет коллекцию **Parameters,** которая состоит из **объектов Parameter.**

Использование метода [Refresh](refresh-method-ado.md) в коллекции **parameters** объекта **Command** извлекает сведения о параметрах поставщика для хранимой процедуры или параметризованного запроса, указанного в **объекте Command.** Некоторые поставщики не поддерживают хранимые вызовы процедур или параметризованные запросы; Вызов метода **Refresh** для коллекции **Parameters** при использовании такого поставщика возвратит ошибку.

Если вы не определили собственные объекты **Parameter** и получили доступ к коллекции **Parameters** перед вызовом метода **Refresh,** ADO автоматически вызывает метод и заполняет коллекцию автоматически.

Вы можете свести к минимуму вызовы поставщика для повышения производительности, если вы знаете свойства параметров, связанных с хранимой процедурой или параметризованный запрос, который требуется вызвать. Используйте метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойств и с помощью метода [Append](append-method-ado.md) добавьте их в коллекцию **Parameters.** Это позволяет устанавливать и возвращать значения параметров без вызова поставщика для сведений о параметре. Если вы пишете поставщику, который не передает сведения о параметрах, необходимо вручную заполнить коллекцию **параметров** с помощью этого метода, чтобы иметь возможность использовать параметры вообще. Используйте метод [Delete,](delete-method-ado-parameters-collection.md) чтобы при необходимости удалить **объекты Parameter** из коллекции **Parameters.**

Объекты в коллекции **Parameters** объекта **Recordset** выходить за пределы области (поэтому становятся недоступными) при закрытии **объекта Recordset.**

