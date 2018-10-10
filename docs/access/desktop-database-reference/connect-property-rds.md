---
title: Connect Property (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb628356e4d93201c38cf84a9c3245b13e044ee3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482511"
---
# <a name="connect-property-rds"></a>Connect Property (RDS)


**Применимо к**: Access 2013 | Office 2013

Указывает имя базы данных, из которой запускаются операций запросов и обновления.

Можно задать свойство **подключение** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде (например, VBScript) сценария.

## <a name="syntax"></a>Синтаксис

Время разработки: \<параметров имя = значение «связь» = «ConnectionString»\>

Во время выполнения: DataControl.Connect = «ConnectionString»

## <a name="parameters"></a>Параметры

  - *ConnectionString*

  - Это допустимая строка подключения. Более общие сведения о строках подключения отображаться со значением свойства [ConnectionString](connectionstring-property-ado.md) или документации поставщика.
    

    > [!NOTE]
    > <P>Указание удаленного MS в качестве поставщика для <STRONG>RDS. DataControl</STRONG> бы создать сценарий четыре уровня. Сценарии, больше, чем три уровня не проверялись и не должно быть необходимым.</P>



  - *DataControl*

  - Объектную переменную, которая представляет **RDS. DataControl** объекта.

