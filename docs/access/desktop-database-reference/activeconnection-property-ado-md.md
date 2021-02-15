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
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="7e872-102">Свойство ActiveConnection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7e872-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="7e872-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e872-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e872-104">Указывает, к каков объекту подключения [ADO](connection-object-ado.md) текущий ячейки или каталог в настоящее время принадлежит.</span><span class="sxs-lookup"><span data-stu-id="7e872-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7e872-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7e872-105">Settings and return values</span></span>

<span data-ttu-id="7e872-106">Задает или возвращает **вариант,** содержащий строку, определяя подключение или **объект Connection.**</span><span class="sxs-lookup"><span data-stu-id="7e872-106">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object.</span></span> <span data-ttu-id="7e872-107">Значение по умолчанию пустое.</span><span class="sxs-lookup"><span data-stu-id="7e872-107">The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e872-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="7e872-108">Remarks</span></span>

<span data-ttu-id="7e872-109">Вы можете установить для этого свойства допустимый объект подключения **ADO** или допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="7e872-109">You can set this property to a valid ADO **Connection** object or to a valid connection string.</span></span> <span data-ttu-id="7e872-110">Если для этого свойства установлена строка подключения, поставщик создает новый объект **Connection** с помощью этого определения и открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="7e872-110">When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="7e872-111">Если для открытия объекта [Cellset](cellset-object-ado-md.md) используется аргумент **ActiveConnection** метода [Open,](open-method-ado-md.md) свойство **ActiveConnection** наследует значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="7e872-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="7e872-112">Если свойству **ActiveConnection** объекта [catalog](catalog-object-ado-md.md) задайте свойство **Nothing,** связанные данные, включая данные в коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанные объекты [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7e872-112">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects.</span></span> <span data-ttu-id="7e872-113">Закрытие объекта **Connection,** который использовался для открытия каталога, имеет тот же эффект, что и установка  **свойству ActiveConnection** свойства **Nothing.**</span><span class="sxs-lookup"><span data-stu-id="7e872-113">Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="7e872-114">Изменение базы данных по умолчанию подключения, на которое ссылается свойство **ActiveConnection** объекта **Catalog,** аннулирует содержимое **каталога.**</span><span class="sxs-lookup"><span data-stu-id="7e872-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="7e872-115">При попытке изменить свойство **ActiveConnection** для открытого объекта **Cellset** произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7e872-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="7e872-116">В Visual Basic не забудьте использовать ключевое слово **Set** при настройке свойства **ActiveConnection** для объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="7e872-116">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object.</span></span> <span data-ttu-id="7e872-117">Если опустить ключевое слово **Set,** фактически будет установлено свойство **ActiveConnection,** равное свойству по умолчанию объекта **Connection,** **ConnectionString.**</span><span class="sxs-lookup"><span data-stu-id="7e872-117">If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**.</span></span> <span data-ttu-id="7e872-118">Код будет работать; однако вы создадим дополнительное подключение к источнику данных, что может отрицательно сказаться на производительности.</span><span class="sxs-lookup"><span data-stu-id="7e872-118">The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="7e872-119">При использовании поставщика данных MSOLAP установите для источника данных в строке подключения имя сервера и уканите в исходном каталоге имя каталога из источника данных.</span><span class="sxs-lookup"><span data-stu-id="7e872-119">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source.</span></span> <span data-ttu-id="7e872-120">Чтобы подключиться к файлу куба, отключенного от сервера, укажете полный путь к этому файлу. ФАЙЛ СДВ.</span><span class="sxs-lookup"><span data-stu-id="7e872-120">To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file.</span></span> <span data-ttu-id="7e872-121">В любом случае установите для поставщика имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="7e872-121">In either case, set the provider to the provider name.</span></span> <span data-ttu-id="7e872-122">Например, следующая строка подключается к каталогу с именем Bobs Video Store на сервере с именем Servername с поставщиком MSOLAP:</span><span class="sxs-lookup"><span data-stu-id="7e872-122">For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="7e872-123">Следующая строка подключается к локальному файлу куба в расположении C: \\ MSDASDK \\ samples \\ oledb \\ olap \\ data \\ bobsvid.cube:</span><span class="sxs-lookup"><span data-stu-id="7e872-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

