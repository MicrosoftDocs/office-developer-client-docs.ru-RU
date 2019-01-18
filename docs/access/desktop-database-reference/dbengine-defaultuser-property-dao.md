---
title: Свойство DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717540"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="a87b2-102">Свойство DBEngine.DefaultUser (DAO)</span><span class="sxs-lookup"><span data-stu-id="a87b2-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="a87b2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a87b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a87b2-104">Задает имя пользователя, используемое для создания **рабочей области** по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="a87b2-104">Sets the user name used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="a87b2-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="a87b2-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87b2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a87b2-106">Syntax</span></span>

<span data-ttu-id="a87b2-107">*выражение* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="a87b2-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="a87b2-108">*выражение* Выражение, возвращающее объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="a87b2-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a87b2-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a87b2-109">Remarks</span></span>

<span data-ttu-id="a87b2-110">Параметр **DefaultUser** имеет тип данных String.</span><span class="sxs-lookup"><span data-stu-id="a87b2-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="a87b2-111">Она может быть 1 — 20 знаков в Microsoft Access рабочих областей и он может включать буквы, диакритические знаки, чисел, пробелов и символов, за исключением: "(кавычки) / (косая черта), \\ (обратная косая черта), \[ \] (квадратные скобки) ,: (двоеточие), | (канал), \< (меньше-знак "больше"), \> (больше-знак "больше"), + (плюс), = (равно входа), (точка с запятой), (разделители)?</span><span class="sxs-lookup"><span data-stu-id="a87b2-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="a87b2-112">(вопросительный знак), \* (звездочка), начальные пробелы и управляющие знаки (ASCII от 00 до ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="a87b2-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="a87b2-113">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="a87b2-113">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="a87b2-114">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="a87b2-114">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="a87b2-115">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="a87b2-115">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="a87b2-116">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="a87b2-116">Weak password: House27.</span></span> <span data-ttu-id="a87b2-117">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="a87b2-117">Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="a87b2-118">По умолчанию, свойство **DefaultUser** имеет значение «администратор» и **DefaultPassword** свойству в строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="a87b2-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="a87b2-119">Имена пользователей не обычно зависят от регистра; Тем не менее при создании повторно учетной записи пользователя, которая была удалена или создана в другой рабочей группе, имя пользователя должно быть точное совпадение с учетом регистра исходного имени.</span><span class="sxs-lookup"><span data-stu-id="a87b2-119">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name.</span></span> <span data-ttu-id="a87b2-120">Пароли зависят от регистра символов.</span><span class="sxs-lookup"><span data-stu-id="a87b2-120">Passwords are case-sensitive.</span></span>

<span data-ttu-id="a87b2-121">Как правило метод **CreateWorkspace** используется для создания объекта **рабочей области** через заданное имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="a87b2-121">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password.</span></span> <span data-ttu-id="a87b2-122">Тем не менее для обеспечения обратной совместимости с предыдущими версиями и для удобства при реализации защищенной базы данных не ядро базы данных Microsoft Access автоматически создает объект **рабочей области** по умолчанию, когда требуется, если он не является open.</span><span class="sxs-lookup"><span data-stu-id="a87b2-122">However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open.</span></span> <span data-ttu-id="a87b2-123">В этом случае значения свойств **DefaultUser** и **DefaultPassword** определить имя пользователя и пароль для объекта **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a87b2-123">In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="a87b2-124">Для этого свойства вступили в силу следует устанавливать до вызова метода любые методы DAO.</span><span class="sxs-lookup"><span data-stu-id="a87b2-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

