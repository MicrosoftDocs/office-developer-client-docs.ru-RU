---
title: Удаление метода (коллекции параметров ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944874"
---
# <a name="delete-method-ado-parameters-collection"></a>Удаление метода (коллекции параметров ADO)


**Применимо к**: Access 2013, Office 2013


Удаляет объект из коллекции [параметров](parameters-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Параметры*. Удаление *индекса*

## <a name="parameters"></a>Параметры

- *Индекс*

  - **Строковое** значение, содержащее имя объекта, который требуется удалить или объекты порядковый номер (индекс) в коллекции.

## <a name="remarks"></a>Примечания

С помощью метода **Delete** в семействе сайтов позволяет удалить один из объектов в коллекции. Этот метод доступен только в коллекции **параметров** объекта [Command](command-object-ado.md) . Необходимо использовать свойство [Name](name-property-ado.md) объекта [параметра](parameter-object-ado.md) или индекса коллекции при вызове метода **Delete** — объектная переменная не является недопустимым.

