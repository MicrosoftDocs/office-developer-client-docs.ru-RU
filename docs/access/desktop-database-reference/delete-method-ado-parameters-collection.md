---
title: Delete Method (ADO Parameters Collection)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482008"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete Method (ADO Parameters Collection)


**Применимо к**: Access 2013 | Office 2013


Удаляет объект из коллекции [параметров](parameters-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Параметры*. Удаление *индекса*

## <a name="parameters"></a>Параметры

  - *Индекс*

  - **Строковое** значение, содержащее имя объекта, который требуется удалить или объекты порядковый номер (индекс) в коллекции.

## <a name="remarks"></a>Замечания

С помощью метода **Delete** в семействе сайтов позволяет удалить один из объектов в коллекции. Этот метод доступен только в коллекции **параметров** объекта [Command](command-object-ado.md) . Необходимо использовать свойство [Name](name-property-ado.md) объекта [параметра](parameter-object-ado.md) или индекса коллекции при вызове метода **Delete** — объектная переменная не является недопустимым.

