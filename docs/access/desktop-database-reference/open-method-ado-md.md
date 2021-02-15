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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288401"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="2abf3-102">Метод Open (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2abf3-102">Open method (ADO MD)</span></span>

<span data-ttu-id="2abf3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2abf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2abf3-104">Извлекает результаты многомерного запроса и возвращает результаты в ячейки.</span><span class="sxs-lookup"><span data-stu-id="2abf3-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abf3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2abf3-105">Syntax</span></span>

<span data-ttu-id="2abf3-106">*Cellset*. Open *Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="2abf3-106">*Cellset*.Open *Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="2abf3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2abf3-107">Parameters</span></span>

|<span data-ttu-id="2abf3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2abf3-108">Parameter</span></span>|<span data-ttu-id="2abf3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2abf3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2abf3-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="2abf3-110">*Source*</span></span> |<span data-ttu-id="2abf3-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="2abf3-111">Optional.</span></span> <span data-ttu-id="2abf3-112">**Вариант,** который оценивает допустимый многомерный запрос, например запрос многомерных выражений (MDX).</span><span class="sxs-lookup"><span data-stu-id="2abf3-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="2abf3-113">Аргумент *Source* соответствует свойству [Source.](source-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2abf3-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="2abf3-114">Дополнительные сведения о MDX см. в документации OLE DB for OLAP в microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="2abf3-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="2abf3-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="2abf3-115">*ActiveConnection*</span></span> |<span data-ttu-id="2abf3-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="2abf3-116">Optional.</span></span> <span data-ttu-id="2abf3-117">Вариант, который оценивается в строку, указывав допустимую переменную объекта ADO [Connection или](connection-object-ado.md) определение для подключения. </span><span class="sxs-lookup"><span data-stu-id="2abf3-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="2abf3-118">Аргумент *ActiveConnection* указывает подключение, в котором необходимо открыть объект [Cellset.](cellset-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2abf3-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="2abf3-119">Если передать определение подключения для этого аргумента, ADO открывает новое подключение с использованием указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="2abf3-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="2abf3-120">Аргумент *ActiveConnection* соответствует свойству [ActiveConnection.](activeconnection-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2abf3-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2abf3-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="2abf3-121">Remarks</span></span>

<span data-ttu-id="2abf3-122">Метод **Open** создает ошибку, если один из его параметров опущен и соответствующее значение свойства не задано перед попыткой открыть **cellset.**</span><span class="sxs-lookup"><span data-stu-id="2abf3-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

