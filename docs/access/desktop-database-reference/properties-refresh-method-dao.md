---
title: Properties.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4df20311746b562d319e371da3cf75b452c064e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480639"
---
# <a name="propertiesrefresh-method-dao"></a>Properties.Refresh Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновление

*выражение* Переменная, которая представляет собой объект- **Свойства** .

## <a name="remarks"></a>Замечания

Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных. Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных. Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .

Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию. Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции. Это гарантирует, что коллекции с самым последним обновлением. С другой стороны с помощью обновления без необходимости может снизить производительность.
