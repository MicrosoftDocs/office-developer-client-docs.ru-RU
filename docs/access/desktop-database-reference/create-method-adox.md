---
title: Создайте метод (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91f5105611df85e007dea6d0e17e3104ea5987a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870256"
---
# <a name="create-method-adox"></a>Создайте метод (ADOX)


**Применимо к**: Access 2013, Office 2013


Создает новый каталог.

## <a name="syntax"></a>Синтаксис

*Каталог*. Создание*стрсоедин*

## <a name="parameters"></a>Параметры

  - *Стрсоедин*

  - **Строковое** значение, используемое для подключения к источнику данных.

## <a name="remarks"></a>Замечания

Метод **Create** создает и открывает новый ADO [подключения](connection-object-ado.md) к источнику данных, указанной в *стрсоедин*. В случае успешной свойству [ActiveConnection](activeconnection-property-adox.md) назначен новый объект **подключения** .

Если поставщик не поддерживает создание новых каталогов, произойдет ошибка.

