---
title: Создание метода (ADOX)
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
# <a name="create-method-adox"></a>Создание метода (ADOX)

**Область применения**: Access 2013, Office 2013

Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание *ConnectString*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectString* |Значение **String,** используемое для подключения к источнику данных.|

## <a name="remarks"></a>Примечания

Метод **Create** создает и открывает новое подключение [ADO](connection-object-ado.md) к источнику данных, указанному в *ConnectString.* В случае успешной работы новый **объект Connection** назначен свойству [ActiveConnection.](activeconnection-property-adox.md)

Ошибка возникает, если поставщик не поддерживает создание новых каталогов.

