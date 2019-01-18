---
title: Метод Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718317"
---
# <a name="create-method-adox"></a>Метод Create (ADOX)

**Применимо к**: Access 2013, Office 2013

Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание*стрсоедин*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*ConnectString* |**Строковое** значение, используемое для подключения к источнику данных.|

## <a name="remarks"></a>Замечания

Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*. В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .

Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.

