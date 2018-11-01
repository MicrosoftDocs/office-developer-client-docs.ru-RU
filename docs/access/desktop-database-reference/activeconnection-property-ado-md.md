---
title: Свойство ActiveConnection (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 2d2ed71f938089d3238eddee91f0c533bba266c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880014"
---
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="205c4-102">Свойство ActiveConnection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="205c4-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="205c4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="205c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="205c4-104">Указывает, какие объект ADO- [подключение](connection-object-ado.md) текущий набор ячеек и каталогов в настоящее время принадлежит.</span><span class="sxs-lookup"><span data-stu-id="205c4-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="205c4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="205c4-105">Settings and return values</span></span>

<span data-ttu-id="205c4-106">Задает или возвращает значение **типа Variant** , содержащее строку, определяющую подключения или объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="205c4-106">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object.</span></span> <span data-ttu-id="205c4-107">Значение по умолчанию будет пустым.</span><span class="sxs-lookup"><span data-stu-id="205c4-107">The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="205c4-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="205c4-108">Remarks</span></span>

<span data-ttu-id="205c4-109">Это свойство можно задать допустимый объект ADO- **подключение** или это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="205c4-109">You can set this property to a valid ADO **Connection** object or to a valid connection string.</span></span> <span data-ttu-id="205c4-110">Если это свойство строки подключения, поставщик создает новый объект **подключения** с помощью этого определения и открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="205c4-110">When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="205c4-111">Если вы используете **ActiveConnection** аргумента метода [Open](open-method-ado-md.md) открыть объект [ячеек](cellset-object-ado-md.md) , свойство **ActiveConnection** наследуют значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="205c4-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="205c4-112">Установка **ActiveConnection** свойства объекта [каталога](catalog-object-ado-md.md) значение **Nothing** освобождает связанных данных, включая данные в коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанных [измерений](dimension-object-ado-md.md), [иерархий](hierarchy-object-ado-md.md)и [уровень](level-object-ado-md.md) и объекты [члена](member-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="205c4-112">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects.</span></span> <span data-ttu-id="205c4-113">Закрытие объект **подключения** , которая использовалась при открытии **каталога** действует как свойства **ActiveConnection** значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="205c4-113">Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="205c4-114">Изменение базы данных по умолчанию подключения ссылается свойство **ActiveConnection** объекта **каталога** нарушает содержимого **каталога**.</span><span class="sxs-lookup"><span data-stu-id="205c4-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="205c4-115">При попытке изменить свойство **ActiveConnection** open объекта **ячеек** , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="205c4-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="205c4-116">В Visual Basic не забудьте ключевого слова **Set** при задании свойства **ActiveConnection** для объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="205c4-116">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object.</span></span> <span data-ttu-id="205c4-117">Если опустить ключевого слова **Set** , вам будет фактически свойства **ActiveConnection** равно объект **подключения** по умолчанию свойства **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="205c4-117">If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**.</span></span> <span data-ttu-id="205c4-118">Код будет работать; Тем не менее будет создать дополнительные подключения к источнику данных, который может иметь негативное влияние.</span><span class="sxs-lookup"><span data-stu-id="205c4-118">The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="205c4-119">При использовании поставщика данных MSOLAP, задайте источника данных в строке подключения с именем сервера и присвоено имя каталога базу данных из источника данных.</span><span class="sxs-lookup"><span data-stu-id="205c4-119">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source.</span></span> <span data-ttu-id="205c4-120">Для подключения к файлу куба, отключены от сервера, задайте расположение полный путь. Файл КУБ.</span><span class="sxs-lookup"><span data-stu-id="205c4-120">To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file.</span></span> <span data-ttu-id="205c4-121">В любом случае значение имени поставщика и имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="205c4-121">In either case, set the provider to the provider name.</span></span> <span data-ttu-id="205c4-122">Например следующую строку подключается к каталогу с именем Bobs видео хранилища на сервере с именем имя сервера с поставщиком MSOLAP:</span><span class="sxs-lookup"><span data-stu-id="205c4-122">For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="205c4-123">Следующая строка подключается к файлу локального куба в расположении C:\\MSDASDK\\примеры\\oledb\\olap\\данные\\bobsvid.cub:</span><span class="sxs-lookup"><span data-stu-id="205c4-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

