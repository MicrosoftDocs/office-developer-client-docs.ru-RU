---
title: Метод Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 866faae5d8c99258075a81f504fa9ce069f4690a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949378"
---
# <a name="create-method-adox"></a>Метод Create (ADOX)

**Применимо к**: Access 2013, Office 2013

Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание*стрсоедин*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Стрсоедин* |**Строковое** значение, используемое для подключения к источнику данных.|

## <a name="remarks"></a>Примечания

Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*. В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .

Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.

