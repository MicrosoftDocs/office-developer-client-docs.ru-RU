---
title: Create Method (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482579"
---
# <a name="create-method-adox"></a>Create Method (ADOX)


**Применимо к**: Access 2013 | Office 2013


Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание*стрсоедин*

## <a name="parameters"></a>Параметры

  - *Стрсоедин*

  - **Строковое** значение, используемое для подключения к источнику данных.

## <a name="remarks"></a>Замечания

Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*. В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .

Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.

