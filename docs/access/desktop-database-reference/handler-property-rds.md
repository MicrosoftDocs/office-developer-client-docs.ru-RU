---
title: Свойство Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb9444091611fbd051da9fa649b5d3efdb92ee6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923583"
---
# <a name="handler-property-rds"></a><span data-ttu-id="929ae-102">Свойство Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="929ae-102">Handler property (RDS)</span></span>


<span data-ttu-id="929ae-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="929ae-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="929ae-104">Указывает имя программы настройки на сервере (обработчик), которая расширяет возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и все параметры, используемые в *обработчик*.</span><span class="sxs-lookup"><span data-stu-id="929ae-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="929ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="929ae-105">Syntax</span></span>

<span data-ttu-id="929ae-106">*DataControl*. Обработчик = *строка*</span><span class="sxs-lookup"><span data-stu-id="929ae-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="929ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="929ae-107">Parameters</span></span>

  - <span data-ttu-id="929ae-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="929ae-108">*DataControl*</span></span>

  - <span data-ttu-id="929ae-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="929ae-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="929ae-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="929ae-110">*String*</span></span>

  - <span data-ttu-id="929ae-111">**Строковое** значение, содержащее имя обработчика и любых параметров, все запятыми (например, «handlerName, parm1, parm2,..., parm *N*»).</span><span class="sxs-lookup"><span data-stu-id="929ae-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="929ae-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="929ae-112">Remarks</span></span>

<span data-ttu-id="929ae-113">Это свойство поддерживает настройки, функциональные возможности, необходимо задать свойство [CursorLocation](cursorlocation-property-ado.md) **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="929ae-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="929ae-114">Имя обработчика и ее параметры при их наличии, разделенных запятыми («,»).</span><span class="sxs-lookup"><span data-stu-id="929ae-114">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="929ae-115">Непредсказуемое поведение приведет к, если точку с запятой («;») в любом месте отображается в *строке*.</span><span class="sxs-lookup"><span data-stu-id="929ae-115">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="929ae-116">Можно создать собственный обработчик условии, что он поддерживает интерфейс **IDataFactoryHandler** .</span><span class="sxs-lookup"><span data-stu-id="929ae-116">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="929ae-117">Имя обработчика по умолчанию — **MSDFMAP. Обработчик**, и его параметр по умолчанию — это файл настройки с именем **MSDFMAP. INI**.</span><span class="sxs-lookup"><span data-stu-id="929ae-117">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="929ae-118">Это свойство используется для вызова настройки альтернативного файлы, созданные администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="929ae-118">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="929ae-119">Альтернатива для установки свойства **обработчика** — указание обработчика и параметры в свойство [ConnectionString](connectionstring-property-ado.md) ; то есть «\**обработчик = \*\*\* handlerName, parm1, parm2,...;*«.</span><span class="sxs-lookup"><span data-stu-id="929ae-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

