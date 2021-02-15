---
title: Свойство CommandText (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296138"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="4cc41-102">Свойство CommandText (ADO)</span><span class="sxs-lookup"><span data-stu-id="4cc41-102">CommandText property (ADO)</span></span>


<span data-ttu-id="4cc41-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cc41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4cc41-104">Указывает текст команды, которая должна быть выдана поставщику.</span><span class="sxs-lookup"><span data-stu-id="4cc41-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4cc41-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4cc41-105">Settings and return values</span></span>

<span data-ttu-id="4cc41-106">Задает или возвращает **строку,** содержаную команду поставщика, например оператор SQL, имя таблицы, относительный URL-адрес или хранимый вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="4cc41-106">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call.</span></span> <span data-ttu-id="4cc41-107">Значение по умолчанию: "" (строка нулевой длины).</span><span class="sxs-lookup"><span data-stu-id="4cc41-107">Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc41-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="4cc41-108">Remarks</span></span>

<span data-ttu-id="4cc41-109">Используйте свойство **CommandText,** чтобы установить или вернуть текст команды, представленной [объектом Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4cc41-109">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="4cc41-110">Обычно это оператор SQL, но также может быть любым другим типом оператора команды, распознаемого поставщиком, например вызовом хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4cc41-110">Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call.</span></span> <span data-ttu-id="4cc41-111">Оператор SQL должен иметь определенный диалект или версию, поддерживаемую обработчиком запросов поставщика.</span><span class="sxs-lookup"><span data-stu-id="4cc41-111">An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="4cc41-112">Если свойство [Prepared](prepared-property-ado.md) объекта **Command** имеет свойство **True** и объект **Command** привязываться к открытому подключению при выполнении свойства **CommandText,** ADO подготавливает запрос (т. е. скомпилную форму запроса, который хранится поставщиком) при вызове методов [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) или **Open.**</span><span class="sxs-lookup"><span data-stu-id="4cc41-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="4cc41-113">В зависимости от [параметра свойства CommandType](commandtype-property-ado.md) ADO может изменить **свойство CommandText.**</span><span class="sxs-lookup"><span data-stu-id="4cc41-113">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property.</span></span> <span data-ttu-id="4cc41-114">Вы можете прочитать свойство **CommandText** в любое время, чтобы увидеть фактический текст команды, который ADO будет использовать во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4cc41-114">You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="4cc41-115">Используйте свойство **CommandText,** чтобы установить или вернуть относительный URL-адрес, который указывает ресурс, например файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="4cc41-115">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory.</span></span> <span data-ttu-id="4cc41-116">Ресурс является относительным расположением, явным образом указанным абсолютным URL-адресом, или неявно открытым [объектом Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4cc41-116">The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="4cc41-117">URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="4cc41-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="4cc41-118">Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="4cc41-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


