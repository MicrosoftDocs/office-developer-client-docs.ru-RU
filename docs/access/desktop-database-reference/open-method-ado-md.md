---
title: Метод Open (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98cceed03af8ba939579d1542421b375e0db64a7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927537"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="93547-102">Метод Open (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="93547-102">Open method (ADO MD)</span></span>


<span data-ttu-id="93547-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93547-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93547-104">Получает результаты запроса многомерных и возвращает результаты для набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="93547-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="93547-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93547-105">Syntax</span></span>

<span data-ttu-id="93547-106">*Набор ячеек*. Откройте*исходный*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="93547-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="93547-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="93547-107">Parameters</span></span>

  - <span data-ttu-id="93547-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="93547-108">*Source*</span></span>

  - <span data-ttu-id="93547-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="93547-109">Optional.</span></span> <span data-ttu-id="93547-110">**Variant** , которое оценивается как допустимый запрос многомерных, например запрос многомерных выражений (MDX).</span><span class="sxs-lookup"><span data-stu-id="93547-110">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="93547-111">*Исходный* аргумент соответствует свойство [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="93547-111">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="93547-112">Дополнительные сведения о многомерных Выражений можно OLE DB для OLAP документация в пакете SDK компонентов доступа к данным Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93547-112">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>

  - <span data-ttu-id="93547-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="93547-113">*ActiveConnection*</span></span>

  - <span data-ttu-id="93547-114">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="93547-114">Optional.</span></span> <span data-ttu-id="93547-115">**Variant** , которое оценивается как строка, задающая допустимое имя переменной объекта ADO- [подключение](connection-object-ado.md) или определения для подключения.</span><span class="sxs-lookup"><span data-stu-id="93547-115">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="93547-116">Аргумент *ActiveConnection* указывает подключения для открытия объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="93547-116">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="93547-117">Если передать определение подключения для этого аргумента ADO откроется новое подключение с помощью указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="93547-117">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="93547-118">Аргумент *ActiveConnection* соответствует свойству [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="93547-118">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="93547-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="93547-119">Remarks</span></span>

<span data-ttu-id="93547-120">Метод **Open** приводит к ошибке, если один из его параметров указан и перед попыткой открыть **ячеек**не задано значение его соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="93547-120">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

