---
title: ������ ������ � ��������� Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807231"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>������ ������ � ��������� Excel

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
���������� ����� �� ������ Microsoft Excel ����� ���� �� ������� �������� ����� ������:
  
- **Numbers**
    
- **Boolean TRUE** ��� **FALSE**
    
- **Strings**
    
- **Errors**
    
� ������� ����� ����� ������� ��������� ������� ���� ����� � �������� ���������� ������� ��� ��� ��������, ������������ ��������� ����� � ������� �������.
  
����� ������������ (��� ��������� ������) ������ ���-�� � ������, Excel �������� ���������������� ���� � ������� ��������� �� ������, ���� ��� �� �������. ���� ���� ���������� �� ���������� �������� (����� �������), Excel �������� ��� ��������� ������� � ������ ��� ��������� (��������� ������� �� ������������). ���� ������ ���������� � ������� **=**, **+** ��� **-**, Excel �������� ���������������� �� ��� �������. ���� ������������ ������������ ��������� ��� ������ ���������������, ��������� ��������� �� ������, � ������ ������������� � ����� ��������������. � ��������� ������ Excel �������� ����������, ������������� � ������� ���������, ����� ������� � �� ���������. 
  
�������� ����������� ����� ������� ����� ����������� ���������. ������� ����������� ������� � ���������� � ����� ������� ����������� (� ������������ ������� ��������). ���� ��������� ��� �������� ������� �� ������� ������������� � ��������� ����, ���������� ���� ������ � ��������� ������ **#VALUE!**. ���� ������ (�� ���������� ���������) �� ������������ ��� �������, ������������ ��� ��� �����, ���������� ���� ������ � ��������� ������ **#NAME?**. 
  
���� ��������� ������ �� ���������� �� � ������ �� ���� ��������, Excel ������� �� � ���������� ��������� �����, �������� ������, ��������, ������� ������, ���������� ��� �������, � �������������� �� ��������������� �������. ��� ����������� � ������������ � ������������� �����������. ���� �� ���� �� ���� ���������� �� ��������, Excel ������������ ��������� ������ ��� ������ � �������� �� � ������ ��� ���������.
  
Excel ������������ � ������ ���� ������, ����� ������� �� ������� �������� ������ �� ��������. Excel ����������� ������ � �������� ������� ����� ��� ������ ���������� ���������� ��� �������, ������� �� ��������� ������ � �������� ����������, ��� ���� ��������� � ������� ������ �������� � ������.
  
Excel ������������� ����������� ��������� ����� ���������� ������ �������� �� ������ �� ������� ����� ������ �� ������ � ������� ������� XLM **EVALUATE** � �� ����������� � API C, **xlfEvaluate**. ��� ������� �������������, ������ �������, ������� ������ ������ ����������� ���������� � ���� DLL. ��� ������� ���������� �� ���������� ���� ��������� ���, ��� ������ ������ ��������� �� ������� ��� ��������� �������������� ����� ��� ���������� ������ **#VALUE!** � ������ ���� ������ ���������. 
  
## <a name="numbers"></a>�����

��� ����� �� ������ Excel �������������� ��� 8-�������� ����� ����� � ��������� ������� (������� ��������). ��� �� �����, ���������� ���� ����� � Excel �� ��������� ������������� ��������� IEEE, ��� �������� � ��������� �������.
  
|**���**|**������������ ��������**|**����������� ��������**|
|:-----|:-----|:-----|
|8-�������� ����� �� ��������� IEEE (������� ��������)  <br/> |1.7976931348623157E + 308  <br/> |2.2250738585072014E-308  <br/> |
|���� (������������ �������� ��� ��������� �������)  <br/> |1.7976931348623157E + 308  <br/> |2.22507385850721E-308  <br/> |
|���� (���� �������)  <br/> |9.99999999999999E + 307  <br/> |2.22507385850721E-308  <br/> |
   
������������� ����� �� ��������� IEEE (�� ���� ����� � ��������� �� 2.2250738585072009E�308 �� 4.9406564584124654E�324) �� �������������� �� ������ Excel, �� �������������� ����� Double � VBA.
  
���� ������� DLL ���������� +/- ������������� �� ��������� IEEE ��� ������������ ����� � ������� ���������, Excel ����������� ��� � �������� **#NUM!**. ��� ������������� ����� � ����� ���� ����������� ������������� ������� � Excel ������������� � ������������� ����. ������������� ���� �� ��������� IEEE ��������������, �� ���� ����� ������������ �������� DLL � ������������ ��� **-0**. (�������� **\<** �� ��������� �������� �� ������������� ����, ������� **=A1\<0** ������������� ��� **TRUE**, ���� ������ A1 �������� ������������� ����). 
  
�������� ��������, ��� ��������� �������� ������� ����� ����� ����� �����������. ��������, ������� ����� ����� �� ����� ���� �������� �������� � ��������� ������� � � ������ ������� ����� ������ ������� ���������, ���� ���� ������ ��������� ������ ���� �����.
  
## <a name="long-unicode-strings"></a>������� ������ �������

��� ������, ������� ������������ ����� � Excel, ��� �� ������ ������� �������� ��� ������ �������. ������ ������� �� ������ ����� ��������� ����� � 32 767 (2<sup>15</sup>��1) �������� � ��������� ����� ������ �������. 
  
����� ������� �������� API C, ������ �� ������ ���� ��������� �������� ������ �� 255 ��������, � API C ������� ��� �����������. � Excel�2007 API C �������� ��� ��������� ������� ����� ������� � Excel. ��� ��������, ��� ������� DLL, ������������������ ���������� ��������, ����� ��������� ��������� ������� � ���������� ������ �������.
  
> [!NOTE]
> [!����������] � ����� �������� ������������� �������� ������ �� ��������� �������������� � API C. ��� �� �����, �� ��� ���������������� �� �� ����������� � 255 ��������. 
  
## <a name="returning-errors"></a>������� ������

Excel ��������� ������ �� ������, ����� �� ������� ������������� ��������� ������� ��� ���������� � ���������� ��� ���� �� ������������ ������� ��� �������� ���. ��� ���� �������� ��������������� ����. ���� ���������� ������� � ���������� �� ������ ����� �������� � �������, ������� �������� ������������ � ���� ����. ���� �������������� ������� ������ ���������� ������, ������������� � ���������� Excel.
  
### <a name="null"></a>#�����!

������ **#NULL!** ������������ ���������� ��������������� ��������� XLM. ��������, ����� **GET.DOCUMENT(78)** ��� ����������� ������� API C **xlfGetDocument** � ���������� 78, ���� ������� �� ����������, �������� � ���� ������. �� ����� ����� ���������� ��������� �������, ����� ���, � �������, ��������� ������ ������. 
  
�� ������ ���������� ��� ������ � ����������� �������������� ��������, ���� ��� ��������� ������ ������� �����������.
  
### <a name="div0"></a>#���/0!

�������� ������� Excel ���������� ������ **#DIV/0!**, ���� ����������� ����� ���� ��� ����� ������� ����, ����� ����������� ��� � Excel ��� ��������, �������� �� ����. ��������� �������, ������� �� ����������� ������� � ��������, ����� ����� ���������� ��� ������. ��������, ������� **AVERAGE** ���������� ��� ������, ���� ������� �� ������� ������ ���������� ������������� � �����. 
  
� ����� �������������� �������� ��� ������ ������� ���������� ������ ��� ����������� ����, ��� ���������� ������� �� ����.
  
### <a name="value"></a>#����!

Excel ���������� ������ **#VALUE!**, �������� ������� ��� ��������� ���������� ������������� � ��������� ���. � ������ ���������� �������, ������� ���������� �������������, ��������  `=LN("X")`, Excel �� �������� ��� �������. ��� ����� ������� ��� �������� � ������� ����������� �������������� �������. 
  
��������� ������� ���������� ��� ������, ���� �������� ���������� ������������� � ���� �������. ��������, �������  `DATEVALUE("30-Feb-2007")` ���������� ��� ������ �������� �� ��, ��� �������� ����� ���������� ���. � ���� ������ ��� �������, ������� ���������� ������ �� ������ ����. ��������� ������� ����� ���������� ��� ������, ���� ���� � ��������� �������� ���������, �������� �������  `FIND("a","xyz")`. 
  
�� ������ ���������� ��� ������ �� ����� �������������� �������, ����� ����������, ��� ��������� ����� ������������ ���, �� ����� ���� ������������� � ���������� ��� ��� ������� �� ������� ���������, ���� ��� �������� ���������� ��� ��������� ����� ���������� ������ **#NUM!**. ��� ������ ����� ������������� ����������, ����� ��������� � ���� ���������� ��� �������� ����� ������������ ����� ��� ������. 
  
### <a name="ref"></a>#������!

Excel ���������� ������ **#REF!** � ���������, ���� ��� ���������� � ������, ��� ������������ ������������� ������ ������� �� �������. ��������, ���� ������ B2 �������� �������  `=A1`, ��� �� ����������� � ������ B1 ��������� ������ ������� **=#REF!**. ��� ������ ����� ��������� � ��������, ������� �������� ������, ������������ � ������� �������� ��������� � ������� ��� ��������� � ������� ������, ������� ��� �����. ��������� ������� ����� ����� ���������� ��� ������, ��������  `OFFSET(A1,-1,-1)`. � ���� ������ ����������� ����� ������, ����������� ������� �������� ������, ������� �������������.
  
���� ���� �������������� ������� ��������� ������ � �������� ����������, ��� ������ ����� ����������, ���� ������ ��������������� ��� ������� �������� ������ ������. � ������� XLOPER/XLOPER12s ������ [���������� ������� � Excel](memory-management-in-excel.md) �����������, ��� ��������� �������, ������� ����� ��������� � ���������� ������ � �������� ����������. 
  
### <a name="name"></a>#���?

Excel ���������� ������ **#NAME?**, ���� ��������� �������� ������, ������� �� ������������ ��� ������� ��� �������� ���. ���� ���� �������������� ������� �������� �������� ������ � ��������� �����, � ��� �� ������, ������������� ���������� ��� ������. 
  
### <a name="num"></a>#�����!

������ �� ���������� �������� � �������������� ������� � Excel ���������� ������ **#NUM!**, ���� ������� �������� ������ ������� �� ������� ����������� ���������, ��������  `LN(0)`. ��� ������ ������������� ���������� � �������������� ��������, ����� ����������, ��� ������� �������� ������ ����������� ��� ������� �� ������� ���������.
  
### <a name="na"></a>#�/�

������ **#N/A** ����� ����������, ��� �������� ��� ����������� ��������� ����������. ��������, ������� ��� � ������� ������� ���������� ���������� ��� ������, ���� ������ ���������� �� �������. ��� ������ ����� ����� ������� � ������� ������� **NA** � ������������ � ������� ������� **ISNA**. ����� �������, ��� ������ ����� ������������ �� ������ ��� ����������� ��������� �������, ��������� � �����������.
  
## <a name="see-also"></a>��. �����



[�������� ���������������� � Excel](excel-programming-concepts.md)
  
[���������������� � �������������� C API � Excel](programming-with-the-c-api-in-excel.md)
  
[������ ����� � ������ ��������� ������� �����](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[���������� �� ������� Excel 2013 XLL SDK API](excel-xll-sdk-api-function-reference.md)
