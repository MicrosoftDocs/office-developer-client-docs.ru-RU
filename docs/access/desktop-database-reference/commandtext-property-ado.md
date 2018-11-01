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
ms.openlocfilehash: 86f69be8ed9216619f10bc70e2c701fb109d0ff5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879307"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="d0738-102">Свойство CommandText (ADO)</span><span class="sxs-lookup"><span data-stu-id="d0738-102">CommandText property (ADO)</span></span>


<span data-ttu-id="d0738-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0738-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0738-104">Указывает текст команды для выдачи с использованием поставщика.</span><span class="sxs-lookup"><span data-stu-id="d0738-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d0738-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d0738-105">Settings and return values</span></span>

<span data-ttu-id="d0738-106">Задает или возвращает **строковое** значение, содержащее команды поставщика, например инструкции SQL, имя таблицы, относительный URL-адрес или вызова хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d0738-106">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call.</span></span> <span data-ttu-id="d0738-107">Значение по умолчанию — «» (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="d0738-107">Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0738-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0738-108">Remarks</span></span>

<span data-ttu-id="d0738-109">Используйте свойство **CommandText** задает или возвращает текст команды, представленного объектом [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d0738-109">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="d0738-110">Обычно это будет инструкции SQL, но также может быть любой тип оператора команду распознаются поставщиком, такие как вызов хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d0738-110">Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call.</span></span> <span data-ttu-id="d0738-111">Оператор SQL должен быть определенного диалект или версия, поддерживаемая обработчик запросов поставщика.</span><span class="sxs-lookup"><span data-stu-id="d0738-111">An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="d0738-112">Если свойство [подготовленных](prepared-property-ado.md) объекта **команды** имеет значение **True** , объект **команды** привязан к открытое подключение, если свойство **CommandText** ADO подготавливает запроса (то есть, скомпилированной формы запроса который хранится поставщиком) при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) или **Open** .</span><span class="sxs-lookup"><span data-stu-id="d0738-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="d0738-113">В зависимости от настройки свойства [CommandType](commandtype-property-ado.md) ADO может изменить свойство **CommandText** .</span><span class="sxs-lookup"><span data-stu-id="d0738-113">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property.</span></span> <span data-ttu-id="d0738-114">Свойство **CommandText** можно прочитать в любое время, чтобы увидеть текст фактические команды, ADO будет использовать во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d0738-114">You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="d0738-115">Используйте свойство **CommandText** задает или возвращает относительный URL-адрес, который задает ресурс, такой как файл или папку.</span><span class="sxs-lookup"><span data-stu-id="d0738-115">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory.</span></span> <span data-ttu-id="d0738-116">Ресурс является относительно местоположения, явно указаны с абсолютный URL-адрес, или неявно open объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d0738-116">The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="d0738-117">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d0738-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d0738-118">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="d0738-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


