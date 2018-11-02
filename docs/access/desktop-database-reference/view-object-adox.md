---
title: Объект View (ADOX - ссылки для настольных баз данных Access)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97376361a9ea5dcd71e3f9ef918a8ec7f1ebb0c0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920762"
---
# <a name="view-object-adox"></a><span data-ttu-id="cdff7-102">Объект View (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cdff7-102">View object (ADOX)</span></span>


<span data-ttu-id="cdff7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdff7-104">Представляет отфильтрованного набора записей или виртуальной таблицы.</span><span class="sxs-lookup"><span data-stu-id="cdff7-104">Represents a filtered set of records or a virtual table.</span></span> <span data-ttu-id="cdff7-105">При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **View** можно использовать для Добавление, удаление или изменение представления.</span><span class="sxs-lookup"><span data-stu-id="cdff7-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdff7-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdff7-106">Remarks</span></span>

<span data-ttu-id="cdff7-107">Представление — виртуальных таблицы, созданный из других баз данных таблицы или представления.</span><span class="sxs-lookup"><span data-stu-id="cdff7-107">A view is a virtual table, created from other database tables or views.</span></span> <span data-ttu-id="cdff7-108">Объект **View** позволяет создать представление без необходимости знать или используйте синтаксис поставщика «Создание ПРЕДСТАВЛЕНИЯ».</span><span class="sxs-lookup"><span data-stu-id="cdff7-108">The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="cdff7-109">Свойства объекта **представления** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cdff7-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="cdff7-110">Определение представления с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="cdff7-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="cdff7-111">Укажите объект ADO **команды** , который можно использовать для добавления, удаления или изменения представлений с помощью свойства [команды](command-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="cdff7-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="cdff7-112">Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="cdff7-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

