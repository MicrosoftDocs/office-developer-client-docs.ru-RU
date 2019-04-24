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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295424"
---
# <a name="create-method-adox"></a>Метод Create (ADOX)

**Область применения**: Access 2013, Office 2013

Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание*коннектстринг*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectString* |**Строковое** значение, используемое для подключения к источнику данных.|

## <a name="remarks"></a>Замечания

Метод **CREATE** создает и открывает новое [Подключение](connection-object-ado.md) ADO к источнику данных, указанному в *коннектстринг*. В случае успешного выполнения новый объект **Connection** назначается свойству [ActiveConnection](activeconnection-property-adox.md) .

Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.

