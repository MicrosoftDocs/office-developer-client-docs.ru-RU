---
title: Свойство Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5869c381c7b449502cc2d28de8eeb214bbfb03d0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928658"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="e3a3d-102">Свойство Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="e3a3d-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="e3a3d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3a3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3a3d-104">Получает или задает выражение, представляющее формулу для вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="e3a3d-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="e3a3d-106">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="e3a3d-106">Version Information</span></span>

<span data-ttu-id="e3a3d-107">Добавлена версия: Access 2010
</span><span class="sxs-lookup"><span data-stu-id="e3a3d-107">Version Added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a3d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3a3d-108">Syntax</span></span>

<span data-ttu-id="e3a3d-109">*выражение* . Выражение</span><span class="sxs-lookup"><span data-stu-id="e3a3d-109">*expression* .Expression</span></span>

<span data-ttu-id="e3a3d-110">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="e3a3d-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a3d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3a3d-111">Remarks</span></span>

<span data-ttu-id="e3a3d-112">В Access 2013 можно создавать поля в таблице, вычисление значений.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="e3a3d-113">Расчеты могут включать значения из полей в одной таблицы, а также встроенных функций доступа.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="e3a3d-114">Расчет не может содержать поля из таблицы или запросы.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="e3a3d-115">Результаты расчета доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="e3a3d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="e3a3d-116">Example</span></span>

<span data-ttu-id="e3a3d-117">Следующий пример демонстрирует создание вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-117">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="e3a3d-118">Метод CreateField создает поле с именем **полное имя**.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-118">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="e3a3d-119">Выражение затем задано значение выражения, вычисляющий значение поля.</span><span class="sxs-lookup"><span data-stu-id="e3a3d-119">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="e3a3d-120">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e3a3d-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

