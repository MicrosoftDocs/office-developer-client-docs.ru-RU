---
title: Метод Open (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703834"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="8fbe6-102">Метод Open (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8fbe6-102">Open method (ADO MD)</span></span>

<span data-ttu-id="8fbe6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fbe6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fbe6-104">Получает результаты запроса многомерных и возвращает результаты для набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbe6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbe6-105">Syntax</span></span>

<span data-ttu-id="8fbe6-106">*Набор ячеек*. Откройте*исходный*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="8fbe6-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="8fbe6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8fbe6-107">Parameters</span></span>

|<span data-ttu-id="8fbe6-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8fbe6-108">Parameter</span></span>|<span data-ttu-id="8fbe6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8fbe6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8fbe6-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="8fbe6-110">*Source*</span></span> |<span data-ttu-id="8fbe6-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-111">Optional.</span></span> <span data-ttu-id="8fbe6-112">**Variant** , которое оценивается как допустимый запрос многомерных, например запрос многомерных выражений (MDX).</span><span class="sxs-lookup"><span data-stu-id="8fbe6-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="8fbe6-113">*Исходный* аргумент соответствует свойство [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbe6-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="8fbe6-114">Дополнительные сведения о многомерных Выражений можно OLE DB для OLAP документация в пакете SDK компонентов доступа к данным Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="8fbe6-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="8fbe6-115">*ActiveConnection*</span></span> |<span data-ttu-id="8fbe6-116">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-116">Optional.</span></span> <span data-ttu-id="8fbe6-117">**Variant** , которое оценивается как строка, задающая допустимое имя переменной объекта ADO- [подключение](connection-object-ado.md) или определения для подключения.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="8fbe6-118">Аргумент *ActiveConnection* указывает подключения для открытия объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbe6-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="8fbe6-119">Если передать определение подключения для этого аргумента ADO откроется новое подключение с помощью указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="8fbe6-120">Аргумент *ActiveConnection* соответствует свойству [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbe6-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8fbe6-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="8fbe6-121">Remarks</span></span>

<span data-ttu-id="8fbe6-122">Метод **Open** приводит к ошибке, если один из его параметров указан и перед попыткой открыть **ячеек**не задано значение его соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="8fbe6-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

