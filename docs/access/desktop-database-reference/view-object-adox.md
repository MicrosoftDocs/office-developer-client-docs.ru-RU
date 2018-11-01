---
title: Объект View (ADOX - ссылки для настольных баз данных Access)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1c3b2cc99cad4ba3b9ee71f0c44ee67b32d41d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873133"
---
# <a name="view-object-adox"></a>Объект View (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет отфильтрованного набора записей или виртуальной таблицы. При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **View** можно использовать для Добавление, удаление или изменение представления.

## <a name="remarks"></a>Замечания

Представление — виртуальных таблицы, созданный из других баз данных таблицы или представления. Объект **View** позволяет создать представление без необходимости знать или используйте синтаксис поставщика «Создание ПРЕДСТАВЛЕНИЯ».

Свойства объекта **представления** можно выполнить следующие действия.

  - Определение представления с помощью свойства [Name](name-property-adox.md) .

  - Укажите объект ADO **команды** , который можно использовать для добавления, удаления или изменения представлений с помощью свойства [команды](command-property-adox.md) .

  - Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

