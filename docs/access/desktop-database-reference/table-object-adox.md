---
title: Объект таблицы (ADOX)
TOCTitle: Table Object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b63014a57104d5d31f5ac5620b26712a9f97347b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869297"
---
# <a name="table-object-adox"></a>Объект таблицы (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет таблицу базы данных, включая столбцов, индексов и ключи.

## <a name="remarks"></a>Замечания

Следующий код создает новую **таблицу**.

`Dim obj As New Table`

С помощью свойств и коллекций объектов **в таблице** можно выполнить следующие действия.

  - Определение таблицы с помощью свойства [Name](name-property-adox.md) .

  - Определите тип таблицы с помощью свойства [типа](https://msdn.microsoft.com/library/jj250042\(v=office.15\)) .

  - Доступ к столбцам базы данных таблицы с помощью коллекции [столбцов](columns-collection-adox.md) .

  - Доступ к индексов таблицы с помощью коллекции [индексов](indexes-collection-adox.md) .

  - Доступ к разделам таблицы с набором [разделов](keys-collection-adox.md) .

  - Укажите [каталог](catalog-object-adox.md) , который несет ответственность за таблицы с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .

  - Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

  - Доступа к свойствам конкретного поставщика в таблице с набором [свойств](properties-collection-ado.md) .


> [!NOTE]
> <P>Поставщик данных может поддерживает все свойства объектов <STRONG>в таблице</STRONG> . Если выбрать значение для свойства, которое не поддерживает поставщик, произойдет ошибка. Для новых объектов <STRONG>в таблице</STRONG> ошибка возникает, когда объект добавляется в коллекцию. Для существующих объектов ошибка возникает, когда для свойства.</P>



При создании объектов **в таблице** , наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство. Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.

