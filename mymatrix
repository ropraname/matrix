import copy
class MyMatrix:
    def __init__(self, data):
        self.__data = copy.deepcopy(data)

        try:
            self.__data != list
        except Exception:
            raise NotImplementedError

    def __repr__(self) -> str:
        data_str = ''
        for i in range(len(self.__data)):
            for j in range(len(self.__data[i])):
                if j < 0:
                    data_str += str(self.__data[i][j]) + ' '
                if j == 0:
                    data_str += str(self.__data[i][j])
                if j > 0:
                    data_str += ' ' + str(self.__data[i][j])
                if i != len(self.__data) - 1 and j+1 == len(self.__data[i]):
                    data_str += '\n'
        return data_str

    def size(self) -> tuple:
        return len(self.__data), len(self.__data[0])

    def flip_up_down(self):
        datac = copy.deepcopy(self.__data)
        for i in range(len(self.__data)):
            for j in range(len(self.__data[i])):
                self.__data[i][j] = datac[-(i+1)][j]

    def flip_left_right(self):
        datac = copy.deepcopy(self.__data)
        for i in range(len(self.__data)):
            for j in range(len(self.__data[i])):
                self.__data[i][j] = datac[i][-(j + 1)]

    # методы flip_ ИЗМЕНЯЮТ матрицу
    # методы flipped_ по сути делают то же самое,
    # но возвращают изменённую КОПИЮ матрицы

    def flipped_up_down(self):
        datatc = copy.deepcopy(self.__data)
        for i in range(len(self.__data)):
            for j in range(len(self.__data[i])):
                datatc[i][j] = self.__data[-(i+1)][j]
        return datatc

    def flipped_left_right(self):
        datatc = copy.deepcopy(self.__data)
        for i in range(len(self.__data)):
            for j in range(len(self.__data[i])):
                datatc[i][j] = self.__data[i][-(j + 1)]
        return datatc

    def transpose(self):
        transposed_data = []
        datac = copy.deepcopy(self.__data)
        for j in range(len(datac[0])):
            tmp = []
            for i in range(len(datac)):
                tmp += [datac[i][j]]
            transposed_data += [tmp]
        self.__data = transposed_data
        return self.__data


        #raise NotImplementedError

    def transposed(self):
        transposed_data = []
        datatc = copy.deepcopy(self.__data)
        for j in range(len(datatc[0])):
            tmp = []
            for i in range(len(datatc)):
                tmp += [datatc[i][j]]
            transposed_data += [tmp]
        datatc = transposed_data
        return datatc
    """
        Return transposed copy of MyMatrix.
    """

