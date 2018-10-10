---
title: Объект View (ADOX - ссылки для настольных баз данных Access)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca58dd83ee3d3675a4ca272e1074b8d8cc930391
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483060"
---
# <a name="view-object-adox"></a>View Object (ADOX)


**Применимо к**: Access 2013 | Office 2013

Представляет отфильтрованного набора записей или виртуальной таблицы. При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **View** можно использовать для Добавление, удаление или изменение представления.

## <a name="remarks"></a>Замечания

Представление — виртуальных таблицы, созданный из других баз данных таблицы или представления. Объект **View** позволяет создать представление без необходимости знать или используйте синтаксис поставщика «Создание ПРЕДСТАВЛЕНИЯ».

Свойства объекта **представления** можно выполнить следующие действия.

  - Определение представления с помощью свойства [Name](name-property-adox.md) .

  - Укажите объект ADO **команды** , который можно использовать для добавления, удаления или изменения представлений с помощью свойства [команды](command-property-adox.md) .

  - Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

