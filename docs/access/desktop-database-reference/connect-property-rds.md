---
title: Свойство (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d9b901f925ccc009a12ef527f7bc857515042c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872405"
---
# <a name="connect-property-rds"></a>Свойство (RDS)


**Применимо к**: Access 2013, Office 2013

Указывает имя базы данных, из которой запускаются операций запросов и обновления.

Можно задать свойство **подключение** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде (например, VBScript) сценария.

## <a name="syntax"></a>Синтаксис

Время разработки: \<параметров имя = значение «связь» = «ConnectionString»\>

Во время выполнения: DataControl.Connect = «ConnectionString»

## <a name="parameters"></a>Параметры

- *ConnectionString*

  - Это допустимая строка подключения. Более общие сведения о строках подключения отображаться со значением свойства [ConnectionString](connectionstring-property-ado.md) или документации поставщика.
    
    > [!NOTE]
    > Указание удаленного MS в качестве поставщика для **RDS. DataControl** бы создать сценарий четыре уровня. Сценарии, больше, чем три уровня не проверялись и не должно быть необходимым.

- *DataControl*

  - Объектную переменную, которая представляет **RDS. DataControl** объекта.

