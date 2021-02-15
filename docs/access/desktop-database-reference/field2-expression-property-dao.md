---
title: Свойство Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292820"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="cfc7b-102">Свойство Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="cfc7b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfc7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfc7b-104">Получает или задает выражение, представляю которое представляет формулу для вычисляемой поля.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="cfc7b-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="cfc7b-106">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="cfc7b-106">Version information</span></span>

<span data-ttu-id="cfc7b-107">Добавлена версия: Access 2010</span><span class="sxs-lookup"><span data-stu-id="cfc7b-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc7b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfc7b-108">Syntax</span></span>

<span data-ttu-id="cfc7b-109">*выражение .* Выражение</span><span class="sxs-lookup"><span data-stu-id="cfc7b-109">*expression* .Expression</span></span>

<span data-ttu-id="cfc7b-110">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc7b-111">Заметки</span><span class="sxs-lookup"><span data-stu-id="cfc7b-111">Remarks</span></span>

<span data-ttu-id="cfc7b-112">В Access 2013 можно создавать поля таблиц, вычисляя значения.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="cfc7b-113">Вычисления могут включать значения из полей в одной таблице, а также встроенные функции Access.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="cfc7b-114">Вычисление не может включать поля из других таблиц или запросов.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="cfc7b-115">Результаты вычислений будут только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="cfc7b-116">Пример</span><span class="sxs-lookup"><span data-stu-id="cfc7b-116">Example</span></span>

<span data-ttu-id="cfc7b-117">В приведенном ниже примере показано, как создать вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-117">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="cfc7b-118">Метод CreateField создает поле с именем **FullName**.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-118">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="cfc7b-119">Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.</span><span class="sxs-lookup"><span data-stu-id="cfc7b-119">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="cfc7b-120">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="cfc7b-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

