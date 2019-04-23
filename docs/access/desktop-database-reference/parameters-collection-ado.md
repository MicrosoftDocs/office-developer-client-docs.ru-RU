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

Содержит все объекты [параметров](parameter-object-ado.md) объекта [Command](command-object-ado.md) .

## <a name="remarks"></a>Замечания

Объект **Command** содержит коллекцию **Parameters** , состоящего из объектов **Parameter** .

При использовании метода [Refresh](refresh-method-ado.md) для коллекции **Parameters** объекта **Command** извлекаются сведения о параметрах поставщика для хранимой процедуры или запроса с параметрами, указанными в объекте **Command** . Некоторые поставщики не поддерживают вызовы хранимых процедур или параметризованные запросы; вызов метода **Refresh** в коллекции **Parameters** при использовании такого поставщика возвратит ошибку.

Если вы не определили собственные объекты **параметров** и хотите получить доступ к коллекции **Parameters** перед вызовом метода **Refresh** , ADO автоматически вызывает метод и заполняет коллекцию.

Вы можете минимизировать количество вызовов поставщика, чтобы увеличить производительность, если вы знаете свойства параметров, связанных с хранимой процедурой или параметризованным запросом, которые необходимо вызвать. Используйте метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойства и используйте метод [append](append-method-ado.md) , чтобы добавить их в коллекцию **Parameters** . Это позволяет задавать и возвращать значения параметров, не выполняя вызов поставщика для сведений о параметре. При записи в поставщик, который не предоставляет сведения о параметрах, необходимо вручную заполнить коллекцию **Parameters** с помощью этого метода, чтобы иметь возможность использовать параметры вообще. Используйте метод [Delete](delete-method-ado-parameters-collection.md) для удаления объектов **Parameter** из коллекции **Parameters** (при необходимости).

Объекты в коллекции **Parameters** объекта **Recordset** выходят из области действия (поэтому становятся недоступными) при закрытии **набора записей** .

