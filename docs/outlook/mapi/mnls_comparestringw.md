---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Последнее изменение: 20 февраля 2012 г.'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576178"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сравнение двух строк Юникод.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Параметры

 _код языка_
  
> [in] Идентификатор языкового стандарта. Параметр _Locale_ [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)подробные определения см.
    
 _dwFlags_
  
> [in] Флаги, следует ли игнорировать регистр и диакритические знаки. Подробные определения в разделе параметр _dwCmpFlags_ [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Указатель для первой строки Юникод для сравнения.
    
 _cch1_
  
> [in] Длина в символах первой строки Юникод, за исключением конечный символ null. Приложение может предоставлять отрицательным значением, если строка символом null. В этом случае функция **MNLS_CompareStringW** определяет продолжительность автоматически. 
    
 _pstr2_
  
> [in] Указатель на втором строку в кодировке Юникод для сравнения.
    
 _cch2_
  
> [in] Длина в символах второй строки Юникод, за исключением конечный символ null. Приложение может предоставлять отрицательным значением, если строка символом null. В этом случае функция определяет продолжительность автоматически.
    
## <a name="return-value"></a>������������ ��������

Возвращает значения, описанного для [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Замечания

Эта функция является [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** принимает те же параметры и имеет то же самое, что и [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

