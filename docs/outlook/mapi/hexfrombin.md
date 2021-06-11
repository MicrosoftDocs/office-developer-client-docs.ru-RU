---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412578"
---
# <a name="hexfrombin"></a><span data-ttu-id="8998e-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="8998e-103">HexFromBin</span></span>

  
  
<span data-ttu-id="8998e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8998e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8998e-105">Преобразует двоичный номер в строковую репрезентацию гексадецимального номера.</span><span class="sxs-lookup"><span data-stu-id="8998e-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8998e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8998e-106">Header file:</span></span>  <br/> |<span data-ttu-id="8998e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8998e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8998e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8998e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8998e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8998e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8998e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8998e-110">Called by:</span></span>  <br/> |<span data-ttu-id="8998e-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="8998e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="8998e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="8998e-112">Parameters</span></span>

 <span data-ttu-id="8998e-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="8998e-113">_pb_</span></span>
  
> <span data-ttu-id="8998e-114">[in] Указатель на двоичные данные, которые необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="8998e-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="8998e-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="8998e-115">_cb_</span></span>
  
> <span data-ttu-id="8998e-116">[in] Размер в bytes двоичных данных, на которые указывает параметр _pb._</span><span class="sxs-lookup"><span data-stu-id="8998e-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="8998e-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="8998e-117">_sz_</span></span>
  
> <span data-ttu-id="8998e-118">[вышел] Указатель на строку ASCII с null-terminated, представляющую двоичные данные в гексадецимальных цифрах.</span><span class="sxs-lookup"><span data-stu-id="8998e-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8998e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8998e-119">Return value</span></span>

<span data-ttu-id="8998e-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="8998e-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8998e-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="8998e-121">Remarks</span></span>

<span data-ttu-id="8998e-122">Функция **HexFromBin** передает указатель на единицу двоичных данных, размер которой указывается _параметром cb._</span><span class="sxs-lookup"><span data-stu-id="8998e-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="8998e-123">Возвращается в строке  _sz_ в пределах (2\*  _cb_)+1 bytes памяти, представление этой двоичной информации в гексадецимальных числах.</span><span class="sxs-lookup"><span data-stu-id="8998e-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="8998e-124">Если значение byte десятичной 10, например, то гексадецимальная строка будет 0A, поэтому один byte преобразуется в два bytes в строке.</span><span class="sxs-lookup"><span data-stu-id="8998e-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

