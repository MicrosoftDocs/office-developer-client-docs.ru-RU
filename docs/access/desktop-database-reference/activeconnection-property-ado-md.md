---
title: Свойство ActiveConnection (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280531"
---
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="3ce94-102">Свойство ActiveConnection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3ce94-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="3ce94-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ce94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ce94-104">Указывает, к каков объектУ ADO [Connection](connection-object-ado.md) текущий ячейки или каталог в настоящее время принадлежит.</span><span class="sxs-lookup"><span data-stu-id="3ce94-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3ce94-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="3ce94-105">Settings and return values</span></span>

<span data-ttu-id="3ce94-106">Задает или возвращает **вариант,** содержащий строку, определяющий объект подключения или **подключения.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-106">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object.</span></span> <span data-ttu-id="3ce94-107">По умолчанию пусто.</span><span class="sxs-lookup"><span data-stu-id="3ce94-107">The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce94-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ce94-108">Remarks</span></span>

<span data-ttu-id="3ce94-109">Это свойство можно настроить на допустимый объект ADO **Connection** или допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="3ce94-109">You can set this property to a valid ADO **Connection** object or to a valid connection string.</span></span> <span data-ttu-id="3ce94-110">Когда это свойство заданной строке подключения, поставщик создает новый объект **Подключения** с помощью этого определения и открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="3ce94-110">When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="3ce94-111">Если для открытия объекта [Cellset](cellset-object-ado-md.md) используется аргумент **ActiveConnection** метода [Open,](open-method-ado-md.md) свойство **ActiveConnection** наследует значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="3ce94-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="3ce94-112">Настройка свойства **ActiveConnection** объекта [Каталога](catalog-object-ado-md.md) в **Nothing** освобождает связанные данные, в том числе данные из коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанные объекты [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="3ce94-112">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects.</span></span> <span data-ttu-id="3ce94-113">Закрытие **объекта Подключения,** который использовался для открытия **каталога,** имеет тот же эффект, что и установка свойства **ActiveConnection** в **Nothing.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-113">Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="3ce94-114">Изменение базы данных по умолчанию подключения, ссылающегося на свойство **ActiveConnection** объекта **Каталог,** аннулирует содержимое **каталога.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="3ce94-115">Ошибка будет возникать при попытке изменить свойство **ActiveConnection** на открытый объект **Cellset.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="3ce94-116">В Visual Basic не забудьте использовать ключевое слово **Set** при настройке свойства **ActiveConnection** для **объекта Подключения.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-116">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object.</span></span> <span data-ttu-id="3ce94-117">Если вы не закроете ключевое слово **Set,** вы фактически  задасте свойство **ActiveConnection,** равное свойству объекта Подключения по **умолчанию, ConnectionString.**</span><span class="sxs-lookup"><span data-stu-id="3ce94-117">If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**.</span></span> <span data-ttu-id="3ce94-118">Код будет работать; однако будет создаваться дополнительное подключение к источнику данных, что может иметь негативные последствия для производительности.</span><span class="sxs-lookup"><span data-stu-id="3ce94-118">The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="3ce94-119">При использовании поставщика данных MSOLAP установите источник данных в строке подключения к имени сервера и установите начальный каталог имени каталога из источника данных.</span><span class="sxs-lookup"><span data-stu-id="3ce94-119">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source.</span></span> <span data-ttu-id="3ce94-120">Чтобы подключиться к файлу куба, отсоединяемом от сервера, установите расположение на полный путь к . ФАЙЛ CUB.</span><span class="sxs-lookup"><span data-stu-id="3ce94-120">To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file.</span></span> <span data-ttu-id="3ce94-121">В любом случае установите поставщику имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="3ce94-121">In either case, set the provider to the provider name.</span></span> <span data-ttu-id="3ce94-122">Например, следующая строка подключается к каталогу с именем Bobs Video Store на сервере с именем Servername с поставщиком MSOLAP:</span><span class="sxs-lookup"><span data-stu-id="3ce94-122">For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="3ce94-123">Следующая строка подключается к локальному файлу куба в расположении C: \\ MSDASDK примеры \\ \\ oledb olap данных \\ \\ \\ bobsvid.cub:</span><span class="sxs-lookup"><span data-stu-id="3ce94-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

