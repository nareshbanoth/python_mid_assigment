# python_mid_assigment



class Logger:

    d = {}

    def shouldprintmesage(self, message, timestamp):

        if message in self.d and self.d[message] <= timestamp:
            self.d[message] += timestamp + 10

        elif message not in self.d:
            self.d[message] = timestamp + 10

        else:
            return False

        return True


#d = {}
logger = Logger()

print(logger.shouldprintmesage('fok',1))
print(logger.shouldprintmesage('bar',2))
print(logger.shouldprintmesage('fok',20))

